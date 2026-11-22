# Wie gut sieht „nichts“ aus? Warum ein Backtest eine Vergleichsbasis ohne Information braucht

_Das Ergebnis eines Backtests sagt wenig, solange Sie nicht wissen, was eine Regel ohne jede Information auf derselben Historie erreicht._

Ein Backtest endet mit einer Zahl. Eine Handelsregel ist über einige Jahre vergangener Preise gelaufen und liegt am Ende vorn. Die natürliche Reaktion ist Freude. Die nützlichere ist eine unspektakuläre Frage: vorn im Vergleich wozu?

Die meisten vergleichen mit null. Liegt die Regel am Ende über ihrem Ausgangspunkt, gilt sie als gut. Doch null ist die falsche Marke, und ein paar Münzen zeigen, warum.

## Ein Raum voller Münzwerfer

Stellen Sie sich hundert Menschen in einem Raum vor. Jeder wirft zehnmal eine Münze und schreibt das Ergebnis auf. Niemand im Raum hat irgendein Geschick im Münzwerfen. Trotzdem wird, wenn die Zettel eingesammelt sind, fast sicher eine Handvoll davon achtmal oder öfter Kopf zeigen. Sortieren Sie die Zettel vom besten zum schlechtesten, und der oberste sieht nach Talent aus.

Es ist kein Talent. So sieht der Beste von hundert aus, wenn gar nichts dahintersteckt.

Die Suche nach einer Handelsregel funktioniert genauso. Man prüft nie nur eine Regel. Man probiert einen längeren Rückblick und einen kürzeren, eine strengere Schwelle und eine lockerere, diesen Ausstieg und jenen. Jede Kombination ist eine weitere Person im Raum. Probieren Sie ein paar Tausend durch, und die beste zeigt auf der durchsuchten Historie ein ansehnliches Ergebnis, ob nun irgendeine von ihnen etwas über Preise weiß oder nicht.

Die Zahl ganz oben auf der Liste beantwortet also die falsche Frage. Sie sagt, wie der beste von vielen Versuchen abgeschnitten hat. Sie sagt nicht, wie viel davon die Suche ohnehin hervorgebracht hätte, ohne dass irgendetwas dahinterstand.

## „Nichts“ mit Absicht bauen

Die Lösung ist, genau das zu messen. Bevor Sie eine Regel beurteilen, bauen Sie eine Fassung von ihr, die unmöglich etwas wissen kann, und schicken sie durch exakt denselben Ablauf.

Dafür gibt es einige gängige Wege. Einer ersetzt die Signale der Regel durch Münzwürfe: dieselbe Anzahl an Einstiegen, zufällig verteilt. Ein anderer behält die Signale der Regel, mischt sie aber in der Zeit, sodass jedes noch vorhanden ist, aber nicht mehr neben den Preisen steht, auf die es reagiert hat. Ein dritter mischt die Zielwerte, an die die Regel angepasst wurde, sodass alles, was sie lernt, aus Rauschen stammt. Die Grundidee hat einen gewöhnlichen Namen: Permutationstest.

Gemeinsam ist ihnen, dass die Verbindung zwischen Signal und Preis absichtlich gekappt wird und alles andere unverändert bleibt. Dieselbe Historie. Dieselben Kosten. Dieselbe Bewertung. Und vor allem dieselbe Suche: Hat der echte Durchlauf ein paar Tausend Einstellungen probiert und die beste behalten, dann probiert auch der Durchlauf ohne Information ein paar Tausend Einstellungen und behält die beste.

Dann sehen Sie nach, was „nichts“ erreicht hat.

## Was die Vergleichsbasis sagt und was nicht

Erstens: „Nichts“ ist selten null. Stellen Sie sich einen erfundenen Markt vor, der über die ganze Strecke langsam gestiegen ist. Dort liegt zufälliges Kaufen am Ende vorn. Stellen Sie sich einen anderen vor, der seitwärts lief, mit Kosten bei jedem Handel. Dort liegt fast alles hinten. Die Vergleichsbasis bewegt sich mit der Historie, und genau deshalb führt eine feste Marke wie null in die Irre.

Zweitens: Einmal mischen genügt nicht. Ein einzelner Durchlauf ohne Information kann durch Zufall hoch oder niedrig ausfallen, wie ein einzelner Münzwerfer. Wiederholen Sie ihn viele Male, und Sie erhalten eine Spanne: wo „nichts“ gewöhnlich landet und wie weit es manchmal reicht. Diese Spanne ist die eigentliche Marke.

Drittens ändert sich, was als Ergebnis zählt. Eine Regel, die innerhalb der Spanne liegt, hat nichts gezeigt, so gut ihre Zahl für sich genommen auch aussieht. Eine Regel, die deutlich außerhalb liegt, hat sich einen zweiten Blick verdient, und nur den. Sie hat eine Prüfung auf einer Strecke der Historie bestanden. Der nächste Schritt ist Historie, die sie nie gesehen hat.

Eine Vergleichsbasis sagt nicht, was eine Regel als Nächstes tut. Sie nimmt Ihnen eine Art der Selbsttäuschung: den besten von vielen Versuchen für eine Entdeckung zu halten. Diese zuerst zu beseitigen lohnt sich, weil man leicht hineingerät und die Kontrolle wenig kostet. Sie hält auch den Aufwand ehrlich: Wer gründlicher sucht, sieht das echte Ergebnis steigen, aber das von „nichts“ steigt mit. Beides gemeinsam steigen zu sehen macht bescheiden, und das ist nützlich.

Das gehört zu dem, was Ultimate Trading System, die Software, die wir bauen, von sich aus tut. Jeder Durchlauf wird mit Stimmen wiederholt, die keine Information tragen, damit die Tafel zeigt, wie gut „nichts“ aussieht, bevor irgendetwas daran gemessen wird. Ein Überlebender tritt dann gegen Historie an, die er nie gesehen hat, gemessen an vier einfacheren Arten, dieselbe Strecke zu handeln. Die kostenlose Probephase braucht kein Konto bei einer Börse, denn Konstruktion und Papierbücher arbeiten mit öffentlichen Daten. Gerechnet wird auf einer eigenen Maschine; gehostet wird nichts: https://ultimate-trading-system.com

Dies ist Software, keine Finanzberatung. Der Handel birgt ein erhebliches Verlustrisiko, und das Bestehen dieser Tests ist keine Garantie für künftige Ergebnisse.

---

From [Ultimate Trading System](https://ultimate-trading-system.com/?ref=github-de): find a trading rule, prove it isn't luck, run it forward. No AI anywhere in what runs.
