# Una palabra para poner a prueba una regla de trading: la disposición sellada (entrenamiento, prueba, retenido, reserva)

_Cuatro partes del historial, cada una con una sola tarea, para que el historial que juzga una regla nunca sea el que la eligió._

Cuando alguien pregunta si una regla de trading es real, la pregunta siguiente es siempre: ¿real sobre qué historial? Una disposición sellada lo responde dividiendo el historial en cuatro partes antes de probar nada, cada una con una sola tarea.

## Entrenamiento

El historial del que aprende la búsqueda. Aquí se ajustan las reglas, así que aquí una regla siempre parece buena. Nada de lo que ocurre en entrenamiento cuenta como prueba.

## Prueba

El historial que se usa para elegir entre las reglas que produjo la búsqueda. No es el historial sobre el que se ajustaron, pero sigue siendo historial sobre el que se tomó una decisión. Cuando se elige la mejor de muchas reglas en prueba, prueba empieza a favorecer a la ganadora.

## Retenido

Historial apartado mientras se tomaban todas las decisiones. Las reglas que sobreviven se juzgan aquí, frente a formas más simples de operar el mismo tramo. Retenido es la primera lectura honesta, pero solo una vez: si se cambia algo por lo que mostró, retenido también ha empezado a elegir.

## Reserva

Un último tramo, que se abre al final de todo, cuando ya se ha decidido lo demás. Es la parte que sigue sin verse cuando ya no queda nada que ajustar. Una regla que aguanta aquí se ha juzgado en historial sobre el que nunca se tomó ninguna decisión.

## Por qué «sellada»

Porque las partes se fijan antes de empezar, y las últimas no se miran antes de tiempo. Si se divide el historial solo en dos y se mira la segunda parte más de una vez, se vuelve a elegir sobre el historial que debía juzgar.

## Dónde lo usamos

Ultimate Trading System, el software que construimos, divide así el historial en su disposición sellada: entrenamiento, prueba, retenido y reserva. El historial que juzga una regla nunca es el que la eligió, y la reserva se mira al final. Además, cada ejecución se repite con votos que no llevan información, para ver primero qué buena parece la «nada». La prueba gratuita no necesita cuenta en ningún exchange. El trabajo se ejecuta en una máquina suya; no hay nada alojado: https://ultimate-trading-system.com

Por qué no basta con apartar un solo tramo, con más detalle: https://telegra.ph/Entrenamiento-prueba-retenido-reserva-por-qué-un-solo-tramo-apartado-no-basta-una-vez-que-se-ha-mirado-11-20

La palabra anterior, determinista: https://telegra.ph/Una-palabra-para-poner-a-prueba-una-regla-de-trading-determinista-11-22

Esto es software, no es asesoramiento financiero. Operar conlleva un riesgo de pérdida considerable, y superar estas pruebas no garantiza resultados futuros.

---

From [Ultimate Trading System](https://ultimate-trading-system.com/?ref=github-es): find a trading rule, prove it isn't luck, run it forward. No AI anywhere in what runs.
