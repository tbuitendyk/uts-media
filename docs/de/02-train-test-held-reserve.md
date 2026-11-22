# Training, Test, Zurückgehalten, Reserve: Warum ein einziger beiseitegelegter Abschnitt nicht genügt, sobald Sie ihn angesehen haben

_Ein beiseitegelegter Abschnitt beurteilt eine Regel nur so lange fair, bis Sie auf sein Ergebnis reagieren. Warum vier Teile besser sind als zwei._

Wer eine Handelsregel an vergangenen Preisen prüft, lernt die erste Lektion schnell. Eine Regel, die auf einem Abschnitt der Historie abgestimmt wurde, sieht auf diesem Abschnitt gut aus, weil sie auf ihn zugeschnitten ist. Also legt man einen Teil der Historie beiseite, stimmt die Regel auf dem Rest ab und prüft sie auf dem Teil, den sie nie gesehen hat. Diesen Teil nennt man meist Out-of-Sample-Daten.

Die Idee ist solide. Sie nutzt sich aber schneller ab, als die meisten erwarten, und zwar durch eine völlig vernünftige Gewohnheit: das Ergebnis ansehen und dann darauf reagieren.

## Wie sich ein beiseitegelegter Abschnitt verbraucht

Ein erfundenes Beispiel. Sie durchsuchen einen Abschnitt der Historie und kommen mit zwanzig Regelkandidaten heraus. Sie lassen alle zwanzig auf dem beiseitegelegten Abschnitt laufen. Die meisten schneiden schlecht ab. Drei schneiden gut ab. Sie behalten die drei und notieren ihre Ergebnisse auf dem beiseitegelegten Abschnitt als Beleg.

Diese Ergebnisse sind nicht mehr sauber. Der beiseitegelegte Abschnitt sollte die Regeln beurteilen. Stattdessen hat er sie ausgewählt. Sie haben diese drei behalten, weil sie dort gut abgeschnitten haben; natürlich schneiden sie dort gut ab.

Mit Münzen wird es deutlich. Geben Sie zwanzig Personen je eine Münze und lassen Sie jede zehnmal werfen. Behalten Sie die drei, bei denen am häufigsten Kopf fiel. Ihre Zettel beeindrucken, und sie würden genauso beeindrucken, wenn jede Münze völlig normal wäre, denn Sie haben nach genau dem ausgewählt, was Sie jetzt bewundern. Lassen Sie dieselben drei noch einmal werfen, und sie sind wieder Durchschnitt.

Dieselbe Abnutzung geschieht auch leiser. Das Ergebnis auf dem beiseitegelegten Abschnitt enttäuscht, also gehen Sie zurück, ändern eine Einstellung und prüfen erneut. Etwas besser. Sie ändern noch eine. Jede dieser Runden ist eine kleine Entscheidung, die mithilfe des beiseitegelegten Abschnitts getroffen wurde. Nach genügend Runden ist die Regel auf ihn ebenso zugeschnitten wie auf den ersten Abschnitt. Es hat nur länger gedauert, und an keiner Stelle ist etwas Unredliches passiert.

Daraus ergibt sich ein Grundsatz, der leicht zu sagen und schwer einzuhalten ist: Die Historie, die eine Regel beurteilt, darf nie die Historie sein, die sie gewählt hat. Sobald ein Abschnitt eine Entscheidung beeinflusst, hat er die Seite gewechselt. Er gehört jetzt zum Auswählen.

## Vier Teile statt zwei

Wenn Ansehen und Auswählen Historie verbrauchen, dann lautet die Antwort: vorab festlegen, welche Historie verbraucht werden darf, und einen Teil zurückbehalten, der gar nicht benutzt wird. Eine mögliche Anordnung teilt die Historie in vier Teile: Training, Test, Zurückgehalten und Reserve.

**Training** und **Test** sind die Arbeitsteile. Hier werden Regeln gefunden, verglichen, nachjustiert und verworfen. Diese Teile dürfen Sie so oft ansehen, wie Sie wollen. Dass sie sich abnutzen, ist vorgesehen, und ein gutes Ergebnis dort sollte niemanden beeindrucken.

**Zurückgehalten** ist Historie, auf der nie eine Wahl getroffen wurde. Hier werden die Überlebenden der ersten beiden Teile beurteilt. Weil auf ihr nichts ausgewählt und nichts nachjustiert wurde, bedeutet ein Ergebnis hier etwas, das ein Ergebnis auf den Arbeitsteilen nicht bedeuten kann.

**Reserve** kommt zuletzt. Es gibt sie wegen des Problems von oben. Sobald Sie das Ergebnis auf Zurückgehalten kennen, sind Sie jemand, der hingesehen hat. Sie könnten versucht sein, etwas nachzujustieren oder einfach nur die Überlebenden weiterzuführen, die auf Zurückgehalten am besten abgeschnitten haben, und das ist wieder der Fehler mit den zwanzig Münzen. Reserve ist die Messung, die nach alldem genommen wird, auf Historie, die noch unberührt ist.

## Den letzten Teil ehrlich halten

Eine Vierteilung hilft nur, wenn sie eingehalten wird. Drei Gewohnheiten leisten den größten Teil der Arbeit.

Legen Sie die Teilung fest, bevor Sie anfangen, und schreiben Sie sie auf. Grenzen, die nach dem Blick auf Ergebnisse verschoben werden, sind ebenfalls Entscheidungen.

Legen Sie vorab fest, was als bestanden gilt. Bleibt eine Regel auf Reserve hinter der Marke zurück, dann ist das ehrliche Ergebnis, dass sie zurückgeblieben ist. Die Versuchung wird sein, es wegzuerklären.

Sehen Sie Reserve genau einmal an. Wer ansieht, nachjustiert und wieder ansieht, hat aus ihr einen weiteren Arbeitsteil gemacht. Dann bleibt nichts mehr, womit sich urteilen ließe.

Auch perfekt eingehalten hat die Teilung eine Grenze. Eine Regel, die auf jedem Teil besteht, hat in der Vergangenheit bestanden. Keine Anordnung alter Preise ersetzt Preise, die es noch nicht gibt. Was die Teilung leistet, ist bescheidener und trotzdem wertvoll: Sie verhindert, dass eine Regel von derselben Historie benotet wird, die sie ausgesucht hat.

Ultimate Trading System, die Software, die wir bauen, teilt die Historie in genau diese vier Teile, Training, Test, Zurückgehalten und Reserve, damit die Historie, die eine Regel beurteilt, nie die Historie ist, die sie gewählt hat. Die Schritte Zurückgehalten und Reserve beurteilen die Überlebenden auf Historie, auf der nie eine Wahl getroffen wurde: zuerst Zurückgehalten, zuletzt Reserve. Die kostenlose Probephase braucht kein Konto bei einer Börse, denn Konstruktion und Papierbücher arbeiten mit öffentlichen Daten. Gerechnet wird auf einer eigenen Maschine; gehostet wird nichts: https://ultimate-trading-system.com

Dies ist Software, keine Finanzberatung. Der Handel birgt ein erhebliches Verlustrisiko, und das Bestehen dieser Tests ist keine Garantie für künftige Ergebnisse.

---

From [Ultimate Trading System](https://ultimate-trading-system.com/?ref=github-de): find a trading rule, prove it isn't luck, run it forward. No AI anywhere in what runs.
