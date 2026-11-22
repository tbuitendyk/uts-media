# Pruebe el instrumento antes de confiar en la lectura: plantar un patrón conocido

_Antes de creer lo que un backtest dice sobre precios reales, compruébelo en un mercado inventado cuya respuesta ya conoce. Cómo se hace y por qué._

Un backtest es un instrumento de medida. Entran una regla y un historial de precios, y sale una lectura. Casi toda la preocupación al probar se la lleva la regla: si está sobreajustada, si el historial era lo bastante largo. Mucha menos se dedica a una pregunta más simple. ¿Funciona el propio instrumento?

La pregunta es justa, porque un proceso de pruebas es software, y el software tiene fallos. Lo incómodo es que el historial real no puede decírselo. Si el proceso dice que una regla es buena, usted no tiene otra forma de saber si la regla es buena o si el proceso se equivoca. No conoce la respuesta correcta. Por eso está probando.

Así que, antes de confiar en él con precios reales, dele un caso en el que sí conozca la respuesta.

## Una balanza y un peso conocido

Nadie confía en una balanza de cocina solo porque muestra un número. Se le pone encima algo de peso conocido y se mira si coincide. Luego se quita el peso y se comprueba que marca cero. Las dos comprobaciones descubren fallos distintos. Una balanza atascada en cero supera la segunda y falla la primera. Una balanza que marca peso sin nada encima falla la segunda.

Un proceso de pruebas puede fallar de esas dos mismas maneras. Puede estar ciego: hay algo real en los datos y no informa de nada. O puede ver cosas: no hay nada en los datos e informa de un hallazgo. En el trading, el segundo fallo es el peligroso, porque un hallazgo es lo que usted esperaba, y las buenas noticias rara vez se comprueban dos veces.

## Plantar un patrón y luego barajarlo

El peso conocido, para un backtest, es un mercado inventado con un patrón escondido a propósito.

Empiece con precios hechos a base de lanzar una moneda: cada hora sube o baja, sin relación alguna entre una hora y la siguiente. Ninguna regla puede encontrar nada ahí, porque no hay nada que encontrar. Después plante algo. Por ejemplo: tras tres subidas seguidas, haga que la hora siguiente suba más veces de las que baja. Usted eligió el patrón, sabe dónde está y sabe con qué fuerza lo puso.

Ahora pase ese mercado inventado por el proceso. No por una copia simplificada ni por un modo especial de prueba. Por el de verdad, de principio a fin, el mismo código que más tarde leerá el historial real. Tiene que encontrar lo que usted plantó.

Si no lo encuentra, algo está roto, y este es el lugar barato para enterarse. Las causas habituales son poco vistosas: señales alineadas con la hora equivocada, un paso que descarta filas sin avisar, una puntuación calculada sobre la columna que no era. Cualquiera de ellas puede borrar un patrón real. Con historial real, usted habría concluido sin más que allí no había nada.

Eso es la mitad de la prueba. Para la otra mitad, tome el mismo mercado inventado y barájelo, de modo que todas las subidas y bajadas sigan ahí, pero en otro orden. El patrón ha desaparecido. Páselo por el mismo proceso. Esta vez tiene que salir vacío.

Si aun así informa de un hallazgo, el proceso está viendo cosas. Una causa clásica es información que se filtra desde el futuro: en algún punto, el cálculo de una hora pudo asomarse a una hora posterior. Una filtración así hace que casi cualquier cosa parezca buena, el ruido incluido. En términos de laboratorio, el mercado con el patrón es un control positivo y el barajado es un control negativo. Un resultado solo se cree cuando los dos se comportan como deben.

## Lo que vale aprobar

Conviene tener claro qué demuestra esto. Demuestra que el instrumento puede ver un patrón del tipo y la fuerza que usted plantó, y que calla cuando no hay ninguno. No dice nada sobre ninguna regla concreta encontrada en historial real, ni sobre lo que una regla así hará después.

Dos detalles deciden si la comprobación significa algo.

Plante algo tenue. Un patrón tan ruidoso como una sirena lo puede encontrar hasta un proceso medio roto. Hágalo más o menos tan débil como lo que esperaría encontrar en datos reales.

Ate el aprobado al código que lo obtuvo. Si cambia el proceso, hay que repetir la comprobación. De lo contrario estará confiando en una balanza que se desmontó y se volvió a montar desde la última vez que se comprobó.

En Ultimate Trading System, el software que construimos, primero se prueba el instrumento. Se coloca un patrón conocido en un mercado inventado y se pasa por el proceso real, que debe encontrarlo mientras sus versiones barajadas salen vacías. Cada versión muestra si ha aprobado. La prueba gratuita no necesita cuenta en ningún exchange, porque Construir y Libros en papel funcionan con datos públicos. El trabajo se ejecuta en una máquina suya; no hay nada alojado: https://ultimate-trading-system.com

Esto es software, no es asesoramiento financiero. Operar conlleva un riesgo de pérdida considerable, y superar estas pruebas no garantiza resultados futuros.

---

From [Ultimate Trading System](https://ultimate-trading-system.com/?ref=github-es): find a trading rule, prove it isn't luck, run it forward. No AI anywhere in what runs.
