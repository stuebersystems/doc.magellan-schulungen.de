# MyMagellan - dezentrale Notenerfassung

MyMagellan ist ein zweitteiliges Werkzeug, das dazu dient Zeugnisnoten und mehr unabhängig von der Magellan-Datenbank zu erfassen und dem Erfasser für ihn gefilterte Daten zur Verfügung zu stellen.

Der erste Teil, das `MyMagellan-Center` ist Teil des `Magellan Administrators` und erstellt Dateien, die rollenbezogen die Daten enthalten, die der Lehrer braucht um Zeugnisdaten zu erfassen. Mit dem `MyMagellan Center` werden später auch die von den Lehrern befüllten Dateien wieder in die Magellan-Datenbank importiert.

`MyMagellan` ist der zweite Teil. Dieses Programm kann auf windows-basierten Rechnern installiert werden und wird von den Lehrern genutzt um die Zeugnisdaten für die unterrichteten Schüler zu erfassen.

**MyMagellan Center**<br/>Administrationstool|**MyMagellan**<br/>Lehrertool
--|--
- Erzeugt aus der Datenbank heraus für Lehrer Dateien, die je nach Rolle des Lehrers (Fachlehrer, Klassenleiter, Tutor) eine unterschiedliche Menge an Daten der Schüler enthält<br/><br/>- zeigt eine Übersicht, wessen Datei erstellt wurde, wessen Datei bereits gefüllt wieder übermittelt wurde, welche Dateien wieder nach Magellan eingelesen wurden<br/><br/>- Liest die von den Lehrern gefüllten Dateien wieder in die Schulverwaltungsdatenbank ein|- Wird von den Lehrern auf dem für die Noteneingabe genutzten Windowsrechner installiert<br/><br/>- Ist das Programm, mit dem der Lehrer seine Notendatei füllt.

## Voraussetzungen

Damit lehrerrollen-bezogene Dateien erstellt werden können, müssen in `Magellan` und im `Magellan Administator` Vorbereitungen getroffen werden.

Vorbereitungen<br/>in Magellan|Vorbereitungen<br/>im Magellan Administrator
--|--
- Schüler brauchen Fachdaten<br/>- Lehrer müssen als Fachlehrer, Klassenleiter oder Tutor markiert werden|- Lehrer müssen Benutzerrechte erhalten<br/>- Lehrer müssen als MyMagellan-Teilnehmer gekennzeichnet werden<br/>- Ablagepfad muss je Teilnehmer vergeben werden<br/>- Dateien müssen erzeugt werden

## Dateien verteilen

Die Dateien werden für Rollen, Abteilungen oder Exportsituation gemeinsam erzeugt, beispielsweise:

* für alle Klassenleiter
* für alle Fachlehrer
* für alle Klassen der Abteilung 1 usw.

Die Dateien könnten an eine im Schulnetzwerk für die Lehrer zugängliche Stelle erzeugt werden, per Mail an die Kollegen versendet werden, per Stick veteilt werden, in einem geschützten Bereich der Schulwebseite zum Download angeboten werden usw.

Bitte beachten Sie unsere ausführliche Anleitung unter: [https://doc.magellan.stueber.de/mymagellancenter/verteilen/](https://doc.magellan.stueber.de/mymagellancenter/verteilen/)

## Dateien befüllen

Die Lehrer müssen MyMagellan auf einem windowsbasierten Rechner installieren, öffnen damit ihre Datei und befüllen sie mit Daten. 
Die ausgefüllte Datei wird wieder an den ursprünglichen Speicherort abgelegt oder auf dem Weg der Bereitstellung zurückübermittelt.

Ein gesondertes [Handbuch](https://doc.mymagellan.stueber.de/noteneingabe/) erläutert die Handhabung.

## Dateien einsammeln

Das MyMagellan Center überwacht die Dateien an der Stelle, an der sie erzeugt wurden. Ist die Datei bearbeitet worden, wird dieser Status in der Liste des MyMagellan-Centers per Symbol sichtbar. 
Befüllte Dateien können mit einer gemeinsamen Aktion in die Datenbank übertragen werden, der Status in der Liste zeigt im Anschluss an, dass die Daten bereits eingelesen wurden.

Das "Einsammeln" wird ausführlich hier beschrieben: [https://doc.magellan.stueber.de/mymagellancenter/einsammeln/](https://doc.magellan.stueber.de/mymagellancenter/einsammeln/)