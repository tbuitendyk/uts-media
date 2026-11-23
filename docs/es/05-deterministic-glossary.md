# Una palabra para poner a prueba una regla de trading: determinista

_Qué significa que una investigación de trading dé la misma respuesta con las mismas entradas, por qué importa y cómo comprobar sus propias herramientas._

Hay una palabra más que aparece siempre que alguien pregunta si una regla de trading es real: determinista. Aquí va en lenguaje llano.

## Qué significa

Una prueba es determinista cuando las mismas entradas dan la misma respuesta, siempre. Los mismos precios, los mismos ajustes y la misma versión de la herramienta producen las mismas operaciones, las mismas puntuaciones y el mismo veredicto, la ejecute hoy o dentro de seis meses, en su máquina o en la de otra persona.

## Por qué importa

Un resultado que no se puede reproducir es un resultado que no se puede comprobar. Si dos ejecuciones de la misma prueba no coinciden, ya no sabe si una regla mejoró por un cambio que usted hizo o porque la herramienta, sin más, respondió distinto esta vez. Cada comparación al poner a prueba una regla, frente a una ejecución sin información, frente a una forma más simple de operar, frente a historial que la regla nunca vio, da por hecho que lo único que cambió es lo que usted cambió.

También importa cuando mira otra persona. Un colega, un revisor o usted mismo dentro de un tiempo deberían poder tomar las mismas entradas y llegar al mismo número. Si no pueden, el número es un relato, no una prueba.

## Qué lo rompe

Cualquier cosa que responda distinto de una llamada a otra: un servicio externo consultado mientras corre la prueba, un ajuste que no se guarda junto al resultado, un historial que se corrige sin avisar, un paso cuyo orden no está fijado. Ninguna de ellas tiene que ser grande para que dos ejecuciones no coincidan.

## Cómo comprobar sus propias herramientas

Ejecute la misma prueba dos veces, sin cambiar nada, y compare los resultados línea a línea. Después pregúntese si cada resultado dice exactamente qué precios, qué ajustes y qué versión lo produjeron. Si no lo dice, no podrá repetirlo más adelante aunque la herramienta en sí sea determinista.

## Dónde lo usamos

Ultimate Trading System, el software que construimos, está hecho así. No hay ninguna IA en nada de lo que funciona: el entrenamiento, la puntuación, la simulación y la ejecución son aritmética sencilla sobre datos de mercado, y las mismas entradas dan la misma respuesta cada vez. Cada conjunto de registros nombra aquel del que procede, de modo que un resultado se puede seguir hasta los precios y los ajustes que lo produjeron, y calcular de nuevo. La prueba gratuita no necesita cuenta en ningún exchange. El trabajo se ejecuta en una máquina suya; no hay nada alojado: https://ultimate-trading-system.com

Las otras cuatro palabras, ejecución sin información, retenido, reserva y patrón plantado, se explican aquí: https://telegra.ph/Cuatro-palabras-para-poner-a-prueba-una-regla-de-trading-ejecución-sin-información-retenido-reserva-patrón-plantado-11-20

Esto es software, no es asesoramiento financiero. Operar conlleva un riesgo de pérdida considerable, y superar estas pruebas no garantiza resultados futuros.

---

From [Ultimate Trading System](https://ultimate-trading-system.com/?ref=github-es): find a trading rule, prove it isn't luck, run it forward. No AI anywhere in what runs.
