# Operar en papel solo sirve de control si sigue el mismo camino que las órdenes reales

_Una ejecución en papel debería mostrar lo que una regla de trading habría hecho con dinero real. Solo puede hacerlo si las señales, las órdenes, los tiempos y los costes siguen el mismo camino. Qué se rompe cuando no es así._

Una regla de trading ha superado su backtest. Antes de poner dinero, se pone a funcionar en papel unas semanas. Si los resultados en papel se parecen a los del backtest, la regla pasa a operar con dinero real. Ese es el plan de casi todo operador prudente, y es un buen plan. Pero descansa en una suposición que es fácil romper sin darse cuenta: que la ejecución en papel hace lo mismo que hará la ejecución real.

En el lenguaje de los experimentos, operar en papel es un control. Un control solo funciona cuando se diferencia de lo real en una sola cosa. Aquí esa única diferencia debería ser que no se mueve dinero. Todo lo demás, desde que llega un precio hasta que se registra una ejecución, debería ser igual.

## Dónde se separan el papel y lo real

Muchos montajes en papel se construyen aparte del sistema real, a menudo con prisa, y difieren en detalles pequeños que se acumulan.

**La señal se calcula de otra manera.** El código del backtest se reutiliza para el papel, pero el sistema real tiene su propia versión, escrita para ir rápido. Una redondea un valor y la otra no. Una usa el cierre de la vela y la otra la última operación unos segundos antes. La mayoría de los días nadie lo nota. Los días que importan, las dos no coinciden.

**Los tiempos son otros.** En papel se suele decidir con la vela cerrada y ejecutar al precio de esa vela. En real, el sistema ve cerrarse la vela, calcula, envía la orden y espera. El precio que obtiene es el de unos segundos o minutos después. Una regla que opera movimientos cortos puede perder casi toda su ventaja en ese hueco, y el papel nunca lo mostrará.

**Las ejecuciones son imaginadas.** En papel se suele dar por hecho que cada orden se ejecuta entera y al precio pedido. Las órdenes reales se ejecutan en parte, tarde o nunca, y las que fallan suelen ser justo las que mejor habrían salido.

**Los costes se omiten o se adivinan.** Comisiones, diferencial y el coste de mantener una posición de un día para otro se dejan fuera con facilidad, o se ponen una vez como número redondo y no se vuelven a revisar.

**Los fallos nunca ocurren.** En papel no hay órdenes rechazadas, ni conexiones perdidas, ni reinicios a mitad de una operación. En real, sí. Cómo se comporta el sistema después de cada uno de ellos es parte de lo que la regla hará de verdad con el dinero, y un papel montado por un camino aparte nunca lo pone a prueba.

Cada una de estas cosas es pequeña por separado. Juntas significan que el papel mide una regla un poco distinta de la que se pondrá en marcha. Y cuando luego los dos no coinciden, nadie sabe si cambió la regla o solo la fontanería.

## Cómo hacer del papel un control honesto

El remedio se dice en una línea: que papel y real sigan un solo camino. El mismo código calcula la señal. El mismo código arma la orden. El mismo reloj decide cuándo. Se aplica el mismo modelo de costes. Solo en el último paso, uno envía la orden a un libro simulado y el otro al exchange. Ese último paso es la única diferencia, y por eso es lo único a lo que se puede atribuir una distancia entre papel y real.

De ahí salen algunas comprobaciones.

- Registre qué decidió el papel, cuándo y a qué precio, en la misma forma en que lo registra lo real. Así se pueden comparar línea por línea, no solo por sus totales.
- Ponga los costes desde el primer día, al nivel que espera pagar, y revíselos cuando ya haya ejecuciones reales.
- No deje que el papel sea más amable que lo real. Si lo real espera al cierre de la vela y luego envía la orden, el papel debe esperar y poner precio de la misma manera.
- Tome un papel que sale mejor que el backtest como un aviso, no como una buena noticia. Casi siempre significa que algo en el camino es demasiado fácil.

Nada de esto dice que la regla sea buena. Un papel fiel de una mala regla sigue siendo una mala regla. Lo que da es una lectura en la que se puede confiar: cuando papel y real son el mismo camino, una diferencia entre ellos es una diferencia del mercado, no de su software.

Así funciona Libros en papel en Ultimate Trading System, el software que construimos: una regla que ha superado sus pruebas se pone en marcha en papel, por el mismo camino que toma el dinero real. Las órdenes reales empiezan solo cuando usted las activa, desde un motor de trading en una máquina que usted elige. La prueba gratuita no necesita cuenta en ningún exchange, porque Construir y Libros en papel funcionan con datos públicos. El trabajo se ejecuta en una máquina suya; no hay nada alojado: https://ultimate-trading-system.com

Esto es software, no es asesoramiento financiero. Operar conlleva un riesgo de pérdida considerable, y superar estas pruebas no garantiza resultados futuros.

---

From [Ultimate Trading System](https://ultimate-trading-system.com/?ref=github-es): find a trading rule, prove it isn't luck, run it forward. No AI anywhere in what runs.
