# Ein Begriff für die Prüfung einer Handelsregel: deterministisch

_Was es heißt, dass eine Handelsuntersuchung bei gleichen Eingaben dieselbe Antwort gibt, warum das zählt und wie man die eigenen Werkzeuge prüft._

Ein weiterer Begriff taucht immer auf, wenn jemand fragt, ob eine Handelsregel echt ist: deterministisch. Hier ist er in schlichter Sprache.

## Was er bedeutet

Ein Test ist deterministisch, wenn gleiche Eingaben jedes Mal dieselbe Antwort geben. Dieselben Preise, dieselben Einstellungen und dieselbe Version des Werkzeugs ergeben dieselben Trades, dieselben Bewertungen und dasselbe Urteil, ob man ihn heute laufen lässt oder in sechs Monaten, auf dem eigenen Rechner oder auf dem eines anderen.

## Warum er zählt

Ein Ergebnis, das sich nicht wiederholen lässt, lässt sich nicht prüfen. Wenn zwei Läufe desselben Tests nicht übereinstimmen, weiß man nicht mehr, ob eine Regel besser wurde, weil man etwas geändert hat, oder weil das Werkzeug diesmal einfach anders geantwortet hat. Jeder Vergleich bei der Prüfung einer Regel, mit einem Durchlauf ohne Information, mit einer einfacheren Art zu handeln, mit Historie, die die Regel nie gesehen hat, setzt voraus, dass sich nur das geändert hat, was man selbst geändert hat.

Er zählt auch, wenn jemand anderes hinschaut. Ein Kollege, ein Prüfer oder man selbst später sollte mit denselben Eingaben zu derselben Zahl kommen. Gelingt das nicht, ist die Zahl eine Geschichte und kein Beleg.

## Was ihn bricht

Alles, was von einem Aufruf zum nächsten anders antwortet: ein externer Dienst, der während des Tests abgefragt wird, eine Einstellung, die nicht mit dem Ergebnis gespeichert wird, Historie, die stillschweigend korrigiert wird, ein Schritt, dessen Reihenfolge nicht festliegt. Nichts davon muss groß sein, damit zwei Läufe auseinandergehen.

## Wie man die eigenen Werkzeuge prüft

Denselben Test zweimal laufen lassen, ohne etwas zu ändern, und die Ergebnisse Zeile für Zeile vergleichen. Dann fragen, ob jedes Ergebnis genau sagt, welche Preise, welche Einstellungen und welche Version es erzeugt haben. Sagt es das nicht, lässt es sich später nicht wiederholen, selbst wenn das Werkzeug an sich deterministisch ist.

## Wo wir ihn verwenden

Ultimate Trading System, die Software, die wir entwickeln, ist so gebaut. In dem, was läuft, steckt keine KI: Training, Bewertung, Simulation und Ausführung sind schlichte Arithmetik auf Marktdaten, und gleiche Eingaben geben jedes Mal dieselbe Antwort. Jeder Datensatz nennt den, aus dem er entstanden ist. So lässt sich ein Ergebnis bis zu den Preisen und Einstellungen zurückverfolgen, die es erzeugt haben, und neu berechnen. Die kostenlose Probephase braucht kein Konto bei einer Börse. Gerechnet wird auf einer eigenen Maschine; gehostet wird nichts: https://ultimate-trading-system.com

Die anderen vier Begriffe, Durchlauf ohne Information, Zurückgehalten, Reserve und gepflanztes Muster, sind hier erklärt: https://telegra.ph/Vier-Begriffe-für-die-Prüfung-einer-Handelsregel-Durchlauf-ohne-Information-Zurückgehalten-Reserve-gepflanztes-Muster-11-20

Dies ist Software, keine Finanzberatung. Der Handel birgt ein erhebliches Verlustrisiko, und das Bestehen dieser Tests ist keine Garantie für künftige Ergebnisse.

---

From [Ultimate Trading System](https://ultimate-trading-system.com/?ref=github-de): find a trading rule, prove it isn't luck, run it forward. No AI anywhere in what runs.
