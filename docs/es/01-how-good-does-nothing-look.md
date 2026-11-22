# ¿Hasta qué punto parece buena la «nada»? Por qué un backtest necesita una referencia sin información

_El resultado de un backtest dice poco hasta saber qué obtiene, en el mismo historial, una regla que no sabe nada. Así se construye esa referencia._

Un backtest, la prueba de una regla de trading sobre precios pasados, termina en un número. La regla recorrió varios años de historial y salió por delante. Lo natural es alegrarse. Lo útil es hacerse una pregunta aburrida: ¿por delante de qué?

Casi todo el mundo compara con cero. Si la regla acabó por encima de donde empezó, se da por buena. Pero cero es la marca equivocada, y unas pocas monedas bastan para verlo.

## Una sala llena de gente lanzando monedas

Imagine a cien personas en una sala. Cada una lanza una moneda diez veces y anota lo que sale. Nadie en la sala tiene habilidad alguna para lanzar monedas. Aun así, al recoger las hojas, es casi seguro que un puñado mostrará ocho caras o más. Ordene las hojas de mejor a peor y la primera parecerá talento.

No es talento. Es el aspecto que tiene el mejor de cien cuando no está pasando nada.

Buscar una regla de trading funciona igual. Nunca se prueba una sola regla. Se prueba una ventana de observación más larga y otra más corta, un umbral más estricto y otro más amplio, esta salida y aquella. Cada combinación es una persona más en la sala. Pruebe unos cuantos miles y la mejor mostrará un resultado vistoso en el historial donde se buscó, sepa o no sepa algo sobre los precios.

Por eso el número que encabeza la lista responde a la pregunta equivocada. Dice cuánto obtuvo el mejor de muchos intentos. No dice cuánto de ese resultado habría producido la búsqueda de todos modos, sin nada detrás.

## Fabricar la «nada» a propósito

La solución es medir eso directamente. Antes de juzgar una regla, se construye una versión de ella que no puede saber nada, y se la hace pasar exactamente por el mismo proceso.

Hay varias maneras corrientes de hacerlo. Una es sustituir las señales de la regla por lanzamientos de moneda: el mismo número de entradas, colocadas al azar. Otra es conservar las señales de la propia regla pero barajarlas en el tiempo, de modo que cada una sigue existiendo, pero ya no está junto a los precios a los que respondía. Una tercera es barajar las etiquetas con las que se ajustó la regla, para que todo lo que aprenda lo aprenda del ruido. La idea general tiene un nombre corriente: prueba de permutación.

Lo que tienen en común es que el vínculo entre señal y precio se corta a propósito y todo lo demás se deja igual. El mismo historial. Las mismas comisiones. La misma puntuación. Y, sobre todo, la misma búsqueda: si la ejecución real probó unos miles de ajustes y se quedó con el mejor, la ejecución sin información prueba unos miles de ajustes y también se queda con el mejor.

Entonces se mira cuánto obtuvo la «nada».

## Lo que la referencia dice y lo que no dice

Primero, la «nada» rara vez vale cero. Imagine un mercado inventado que subió poco a poco durante todo el tramo. Allí, comprar al azar termina por delante. Imagine otro que se movió de lado, con una comisión en cada operación. Casi todo termina por detrás. La referencia se mueve con el historial, y justo por eso engaña una marca fija como cero.

Segundo, con barajar una vez no basta. Una sola ejecución sin información puede salir alta o baja por suerte, igual que una sola persona con su moneda. Repítala muchas veces y obtendrá un abanico: dónde suele caer la «nada» y hasta dónde llega a veces. Ese abanico es la marca de verdad.

Tercero, cambia lo que cuenta como resultado. Una regla que queda dentro del abanico no ha mostrado nada, por bueno que parezca su número visto a solas. Una regla que queda claramente fuera se ha ganado una segunda mirada, y nada más. Ha superado una prueba en un tramo del historial. El paso siguiente es historial que nunca ha visto.

Una referencia no dice qué hará una regla después. Elimina una manera de engañarse: confundir el mejor de muchos intentos con un hallazgo. Conviene eliminarla primero, porque es fácil caer en ella y barato comprobarla. Además mantiene honesto el esfuerzo: si se busca con más empeño, el resultado real sube, pero también sube el de la «nada». Ver subir a los dos juntos es una lección de humildad, y sirve.

Es una de las cosas que hace por sí solo Ultimate Trading System, el software que construimos. Cada ejecución se repite con votos que no llevan información, así que el tablero muestra qué buena parece la «nada» antes de juzgar nada frente a ella. Una superviviente se enfrenta luego a historial que nunca vio, medida frente a cuatro maneras más simples de operar el mismo tramo. La prueba gratuita no necesita cuenta en ningún exchange, porque Construir y Libros en papel funcionan con datos públicos. El trabajo se ejecuta en una máquina suya; no hay nada alojado: https://ultimate-trading-system.com

Esto es software, no es asesoramiento financiero. Operar conlleva un riesgo de pérdida considerable, y superar estas pruebas no garantiza resultados futuros.

---

From [Ultimate Trading System](https://ultimate-trading-system.com/?ref=github-es): find a trading rule, prove it isn't luck, run it forward. No AI anywhere in what runs.
