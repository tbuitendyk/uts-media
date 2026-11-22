# Erst das Instrument prüfen, dann der Messung trauen: ein bekanntes Muster pflanzen

_Bevor Sie glauben, was ein Backtest über echte Preise sagt, prüfen Sie ihn an einem erfundenen Markt, dessen Antwort Sie schon kennen._

Ein Backtest ist ein Messinstrument. Eine Regel und ein Stück Historie gehen hinein, ein Messwert kommt heraus. Die meiste Sorge beim Testen gilt der Regel: Ist sie überangepasst, war die Historie lang genug? Viel weniger gilt einer schlichteren Frage. Funktioniert das Instrument selbst?

Die Frage ist berechtigt. Die Verarbeitung dahinter, also die ganze Kette von Rechenschritten zwischen Preisen und Ergebnis, ist Software, und Software hat Fehler. Das Unangenehme daran: Echte Historie kann es Ihnen nicht sagen. Wenn die Verarbeitung meldet, eine Regel sei gut, haben Sie keinen unabhängigen Weg herauszufinden, ob die Regel gut ist oder die Verarbeitung falsch rechnet. Sie kennen die richtige Antwort nicht. Deshalb testen Sie ja.

Geben Sie ihr also, bevor Sie ihr bei echten Preisen trauen, einen Fall, bei dem Sie die Antwort kennen.

## Eine Waage und ein bekanntes Gewicht

Niemand traut einer Küchenwaage nur, weil sie eine Zahl anzeigt. Man legt etwas mit bekanntem Gewicht darauf und sieht nach, ob sie zustimmt. Dann nimmt man es herunter und prüft, ob sie null anzeigt. Die beiden Prüfungen finden verschiedene Fehler. Eine Waage, die bei null festhängt, besteht die zweite und fällt bei der ersten durch. Eine Waage, die ohne Last ein Gewicht anzeigt, fällt bei der zweiten durch.

Die Verarbeitung hinter einem Backtest kann auf dieselben zwei Arten versagen. Sie kann blind sein: In den Daten steckt etwas Echtes, und sie meldet nichts. Oder sie sieht Dinge: In den Daten steckt nichts, und sie meldet einen Fund. Im Handel ist die zweite Art die gefährliche, denn einen Fund haben Sie sich erhofft, und gute Nachrichten werden selten zweimal geprüft.

## Ein Muster pflanzen, dann mischen

Das bekannte Gewicht ist bei einem Backtest ein erfundener Markt, in dem absichtlich ein Muster versteckt wurde.

Beginnen Sie mit Preisen aus Münzwürfen: jede Stunde auf oder ab, ohne dass eine Stunde mit der nächsten zusammenhängt. Dort kann keine Regel etwas finden, weil es nichts zu finden gibt. Dann pflanzen Sie etwas hinein. Zum Beispiel: Nach drei Anstiegen in Folge steigt die nächste Stunde öfter, als sie fällt. Sie haben das Muster gewählt, Sie wissen, wo es steckt, und Sie wissen, wie stark Sie es gemacht haben.

Nun schicken Sie diesen erfundenen Markt durch die Verarbeitung. Nicht durch eine vereinfachte Kopie und nicht durch einen besonderen Testmodus. Durch die echte, von Anfang bis Ende, denselben Code, der später echte Historie liest. Sie muss finden, was Sie gepflanzt haben.

Findet sie es nicht, ist etwas kaputt, und hier erfahren Sie es am billigsten. Die üblichen Ursachen sind unscheinbar: Signale, die an der falschen Stunde ausgerichtet sind, ein Schritt, der stillschweigend Zeilen verwirft, eine Bewertung, die auf der falschen Spalte berechnet wird. Jede davon kann ein echtes Muster auslöschen. Bei echter Historie hätten Sie schlicht geschlossen, dass dort nichts ist.

Das ist die halbe Prüfung. Für die andere Hälfte nehmen Sie denselben erfundenen Markt und mischen ihn, sodass jedes Auf und Ab noch vorhanden ist, aber in anderer Reihenfolge. Das Muster ist weg. Schicken Sie das durch dieselbe Verarbeitung. Diesmal muss sie leer ausgehen.

Meldet sie trotzdem einen Fund, sieht die Verarbeitung Dinge. Eine klassische Ursache ist Information, die aus der Zukunft durchsickert: Irgendwo durfte die Rechnung für eine Stunde einen Blick auf eine spätere Stunde werfen. Ein solches Leck lässt fast alles gut aussehen, auch Rauschen. In der Sprache des Labors ist der Markt mit dem Muster eine Positivkontrolle und der gemischte eine Negativkontrolle. Geglaubt wird ein Ergebnis erst, wenn sich beide richtig verhalten.

## Was ein bestandener Test wert ist

Machen Sie sich klar, was das beweist. Es zeigt, dass das Instrument ein Muster der Art und Stärke sehen kann, die Sie gepflanzt haben, und dass es still bleibt, wenn keines da ist. Es sagt nichts über irgendeine bestimmte Regel, die in echter Historie gefunden wurde, und nichts darüber, was eine solche Regel als Nächstes tut.

Zwei Einzelheiten entscheiden, ob die Prüfung etwas bedeutet.

Pflanzen Sie etwas Schwaches. Ein Muster, laut wie eine Sirene, findet auch eine halb kaputte Verarbeitung. Machen Sie es ungefähr so schwach wie das, was Sie in echten Daten zu finden hoffen.

Binden Sie das Bestehen an den Code, der es erreicht hat. Ändern Sie die Verarbeitung, muss die Prüfung wiederholt werden. Sonst trauen Sie einer Waage, die seit der letzten Kontrolle zerlegt und wieder zusammengesetzt wurde.

In Ultimate Trading System, der Software, die wir bauen, wird das Instrument zuerst geprüft. Ein bekanntes Muster wird in einen erfundenen Markt gepflanzt und durch die echte Verarbeitung geschickt, die es finden muss, während gemischte Versionen davon leer ausgehen. Jede Version zeigt, ob sie bestanden hat. Die kostenlose Probephase braucht kein Konto bei einer Börse, denn Konstruktion und Papierbücher arbeiten mit öffentlichen Daten. Gerechnet wird auf einer eigenen Maschine; gehostet wird nichts: https://ultimate-trading-system.com

Dies ist Software, keine Finanzberatung. Der Handel birgt ein erhebliches Verlustrisiko, und das Bestehen dieser Tests ist keine Garantie für künftige Ergebnisse.

---

From [Ultimate Trading System](https://ultimate-trading-system.com/?ref=github-de): find a trading rule, prove it isn't luck, run it forward. No AI anywhere in what runs.
