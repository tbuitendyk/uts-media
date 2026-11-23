# Papierhandel ist nur dann eine Kontrolle, wenn er denselben Weg nimmt wie echte Orders

_Ein Lauf auf Papier soll zeigen, was eine Handelsregel mit echtem Geld getan hätte. Das kann er nur, wenn Signale, Orders, Zeitpunkte und Kosten denselben Weg nehmen. Was bricht, wenn nicht._

Eine Handelsregel hat ihren Backtest bestanden. Bevor Geld hineingeht, läuft sie ein paar Wochen auf Papier. Sehen die Ergebnisse auf Papier aus wie der Backtest, geht die Regel live. So planen die meisten sorgfältigen Trader, und es ist ein guter Plan. Aber er ruht auf einer Annahme, die leicht bricht, ohne dass es jemand merkt: dass der Lauf auf Papier dasselbe tut wie später der Lauf mit echtem Geld.

In der Sprache des Experiments ist Papierhandel eine Kontrolle. Eine Kontrolle taugt nur, wenn sie sich in genau einer Sache vom Echten unterscheidet. Hier sollte diese eine Sache sein, dass kein Geld fließt. Alles andere, vom Eintreffen eines Preises bis zur verbuchten Ausführung, sollte gleich sein.

## Wo Papier und Echtgeld auseinanderlaufen

Viele Papier-Aufbauten entstehen getrennt vom echten System, oft in Eile, und unterscheiden sich in kleinen Dingen, die sich summieren.

**Das Signal wird anders berechnet.** Der Backtest-Code wird für Papier weiterverwendet, aber das echte System hat eine eigene, auf Tempo geschriebene Fassung. Die eine rundet einen Wert, die andere nicht. Die eine nimmt den Schlusskurs der Kerze, die andere den letzten Handel ein paar Sekunden davor. An den meisten Tagen fällt das niemandem auf. An den Tagen, auf die es ankommt, sind sich beide uneins.

**Die Zeitpunkte sind andere.** Auf Papier wird oft auf der fertigen Kerze entschieden und zu deren Preis ausgeführt. Im echten Betrieb sieht das System die Kerze schließen, rechnet, schickt die Order und wartet. Es bekommt den Preis von einigen Sekunden oder Minuten später. Eine Regel, die kurze Bewegungen handelt, kann in dieser Lücke fast ihren ganzen Vorteil verlieren, und das Papier zeigt es nie.

**Die Ausführungen sind erdacht.** Auf Papier wird meist angenommen, jede Order werde vollständig und zum gewünschten Preis ausgeführt. Echte Orders werden teilweise, spät oder gar nicht ausgeführt, und gerade die verpassten wären oft die besten gewesen.

**Die Kosten fehlen oder sind geschätzt.** Gebühren, Spread und die Kosten, eine Position über Nacht zu halten, lassen sich leicht weglassen oder einmal als runde Zahl eintragen und nie wieder prüfen.

**Die Störungen passieren nie.** Auf Papier gibt es keine abgelehnte Order, keine abgerissene Verbindung, keinen Neustart mitten im Handel. Im echten Betrieb gibt es sie. Wie sich das System danach verhält, gehört zu dem, was die Regel mit echtem Geld tatsächlich tut, und ein Papier auf eigenem Weg prüft das nie.

Jedes dieser Dinge ist für sich klein. Zusammen heißen sie, dass das Papier eine etwas andere Regel misst als die, die live gehen wird. Und wenn beide sich dann widersprechen, kann niemand sagen, ob sich die Regel geändert hat oder nur die Leitungen.

## Wie Papier zu einer ehrlichen Kontrolle wird

Die Abhilfe passt in einen Satz: Papier und Echtgeld nehmen einen einzigen Weg. Derselbe Code berechnet das Signal. Derselbe Code baut die Order. Dieselbe Uhr entscheidet, wann. Dasselbe Kostenmodell gilt. Erst im letzten Schritt geht die Order einmal an ein simuliertes Buch und einmal an die Börse. Dieser letzte Schritt ist der einzige Unterschied, und deshalb ist er das Einzige, dem man einen Abstand zwischen Papier und Echtgeld zuschreiben kann.

Daraus folgen ein paar Prüfungen.

- Halten Sie fest, was das Papier entschieden hat, wann und zu welchem Preis, in derselben Form, in der es der echte Betrieb festhält. Dann lassen sich beide Zeile für Zeile vergleichen, nicht nur in der Summe.
- Rechnen Sie die Kosten vom ersten Tag an ein, in der Höhe, die Sie erwarten, und prüfen Sie sie erneut, sobald es echte Ausführungen gibt.
- Lassen Sie das Papier nicht freundlicher sein als den echten Betrieb. Wartet dieser auf den Kerzenschluss und schickt dann die Order, muss das Papier ebenso warten und ebenso bepreisen.
- Nehmen Sie ein Papier, das besser aussieht als der Backtest, als Warnung, nicht als gute Nachricht. Meist heißt es, dass etwas auf dem Weg zu leicht ist.

Nichts davon sagt, dass die Regel gut ist. Ein treues Papier einer schlechten Regel bleibt eine schlechte Regel. Was es liefert, ist eine Messung, der man trauen kann: Sind Papier und Echtgeld derselbe Weg, dann ist ein Unterschied zwischen ihnen ein Unterschied im Markt, nicht in Ihrer Software.

So arbeiten die Papierbücher in Ultimate Trading System, der Software, die wir bauen: Eine Regel, die ihre Prüfungen bestanden hat, läuft auf Papier vorwärts, auf demselben Weg, den echtes Geld nimmt. Echte Orders beginnen erst, wenn Sie sie einschalten, von einer Handels-Engine auf einem Rechner Ihrer Wahl. Die kostenlose Probephase braucht kein Konto bei einer Börse, denn Konstruktion und Papierbücher arbeiten mit öffentlichen Daten. Gerechnet wird auf einer eigenen Maschine; gehostet wird nichts: https://ultimate-trading-system.com

Dies ist Software, keine Finanzberatung. Der Handel birgt ein erhebliches Verlustrisiko, und das Bestehen dieser Tests ist keine Garantie für künftige Ergebnisse.

---

From [Ultimate Trading System](https://ultimate-trading-system.com/?ref=github-de): find a trading rule, prove it isn't luck, run it forward. No AI anywhere in what runs.
