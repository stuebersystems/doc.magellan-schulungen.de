# M03 - MAGELLAN Administrator

Diese Unterlagen fassen die in der Schulung MAGELLAN-Administrator behandelten Themen zusammen. Eine umfangreichere Dokumentation zu Magellan bietet Ihnen das [Benutzerhandbuch](http://doc.magellan7.stueber.de).

|Hinweis | Bemerkung|
|-- | --|
|**Dauer:** | 6 x 45 min|
|**Inhalt:** | - Installation, Deinstallation, Updates<br/>- neue Datenbank einrichten<br/>- Datenaustausch über das Magellan-Importformat<br/>- Schlüsselverzeichnisse <br/>- Benutzerverwaltung<br/>- Sicherung und Datenbankpflege<br/>- Erstellen von MyMagellan-Dateien mit dem MyMagellan-Center|
|**Zielgruppe:** | Schuladministratoren|
|**Ablauf**:|09:30 – 11:00 Uhr  <br/>11:15 – 12:45 Uhr<br/>13:30 - 14:15 Uhr|

## Installation

!!! info "Hinweis"

     Bitte beachten Sie die ausführliche Beschreibung der [Installation](https://doc.magellan7.stueber.de/schulverwaltung/installation/). 

### Systemvoraussetzungen

Quelle: [https://doc.magellan7.stueber.de/schulverwaltung/installation/systemvoraussetzungen/](https://doc.magellan7.stueber.de/schulverwaltung/installation/systemvoraussetzungen/)
|MAGELLAN| Kompatibilität|
--|--|
|**Betriebssystem 32-Bit**|Windows  Vista / Windows  2008 / Windows  7 / Windows  8 / Windows  10 |
|**Betriebssystem 64-Bit**|Windows 7 /8/10/  Windows 8 /  Windows 10 /  Windows2008 /  Windows 2012 /  Windows 2016 |
|**Office-Versionen**|Office  2007<br/>Office 2010<br/>Office 2013<br/>Office 2016|
|**Hardware**|MAGELLAN benötigt keine besonderen Hardware-Anforderungen|
|**Bildschirmauflösung**|Die Bildschirmauflösung sollte 1280x800 Bildpunkte nicht unterschreiten|

### Erstinstallation von MAGELLAN

Dieser Abschnitt beschreibt die Installation von MAGELLAN mit den einzelnen Installationsschritten und Installationsarten. Bitte beachten Sie die Systemvoraussetzungen.

* Installation von Firebird
* Installation von MAGELLAN
* Serverinstallation
* Arbeitsplatzinstallation
* Einzelplatzinstallation
* Magellan 7 starten nach Neuinstallation

### Installation von Firebird

Laden Sie bitte das Firebird-Installationspaket von [aus dem Downloadbereich unserer Webseiten](http://magellan.stueber.de/download.php). Starten Sie anschließend die Firebird Installation durch einen Doppelklick auf die Datei ``Firebird-2.5.....Win32.exe``. Bitte übernehmen Sie im daraufhin startenden Installationsassistenten auf der Karte `Komponenten auswählen` die voreingestellten Optionen.

!!! warning "Wichtig"

    Bitte verwenden Sie keine abweichende Firebird-Version, sondern setzen die Ausgabe ein, die wir im Downloadbereich unserer Webseite zur Verfügung stellen!

Auf der Karte `Zusätzliche Aufgaben auswählen` übernehmen Sie bitte die Optionen und aktivieren zusätzlich das Häkchen `Die Firebird Client-Bibliothek ins Systemverzeichnis kopieren`.

!!! info "Hinweis"

    Firebird soll nur dem Rechner installiert werden, auf dem zukünftig die Datenbank gespeichert wird. Das kann Ihr Server sein oder auch ein netzwerkunabhängiger Rechner.
    
    Firebird nutzt für den Datenverkehr den Port 3050, mitunter ist dieser Port durch die Windows Firewall gesperrt. Richten Sie bitte eine Ausnahme (Eingehende und Ausgehende Regel) für diesen Port ein.

### Installation von MAGELLAN

Laden Sie bitte das MAGELLAN-Installationspaket [aus dem Downloadbereich unserer Webseiten](http://magellan.stueber.de/download.php). Starten Sie anschließend die Installation per Doppelklick auf die Datei ``Magellan6.msi``.

Der Setup Assistent von Magellan 7 wird gestartet und die Installationsdateien werden entpackt.

Wählen Sie die gewünschte Installationsart aus:

Auswahl|Was passiert?
---|---
**Server** |Der Datenbank-Server (Firebird) und alle weiteren Module werden auf einem Server installiert. Auf diesen befindet sich im Regelfall die Magellan 7 Datenbank. Die einzelnen Arbeitsstationen, welche auf den Server zugreifen, werden mit der Art `Arbeitsplatz` installiert.
**Einzelplatz** |Der Datenbank-Server und alle weiteren Module werden auf einem Rechner installiert. Sie entspricht der Serverinstallation im Netz und wird daher über die gleiche Option ausgewählt.
**Arbeitsplatz** |Es wird ein Arbeitsplatz in Netzwerk installiert. Dazu werden nur die Anwendungsdaten und der Datenbank-Client installiert, jedoch nicht Datenbank, Berichte oder Skripte. Eine Arbeitsplatzinstallation setzt eine Serverinstallation voraus. Firebird darf auf diesem Arbeitsplatz nicht installiert sein.

Die weiteren Beschreibungen finden Sie in den nachfolgenden Abschnitten `Serverinstallation`, `Arbeitsplatzinstallation` und `Einzelplatzinstallation`.

!!! info "Hinweis"

    Die Installation des Datenbankservers (Firebird) wird für die Installationsart `Server-/ Einzelplatzinstallation` vorausgesetzt.

### Serverinstallation

Nachdem Sie die Installationsart `Server bzw. Einzelplatz` gewählt haben, ist der Setup Assistent bereit, die Installation der Dateien vorzunehmen. Die Installation selbst muss direkt auf dem Server erfolgen.

1. Wählen Sie zunächst den Speicherort für die Programmdateien aus.
2. Wählen Sie den Speicherort für die Datenbank und klicken Sie auf `Weiter`.
3. Wählen Sie den Speicherort für die Datenordner (Berichte-, Dokumente-, Importe-, Skripte- und Vorlagenordner) und klicken Sie auf `Weiter`.
4. Klicken Sie nun auf `Installieren`, um mit der Installation zu beginnen.
5. Die Installation selbst kann einige Minuten in Anspruch nehmen. Klicken Sie zum Abschließen der Installation auf `Fertigstellen`.

#### Speicherorte der Anwendungsdaten, Allgemeinen Einstellungs- und Lizenzdateien und der Datenordner

Nach Abschluss der Installation befinden sich standardmäßig die Dateien in folgenden Ordnern auf dem Server:

Anwendungsdaten (z.B. Magellan.exe):

|Betriebssystem | Pfad|
|--------------------| -------------|
|Windows 7 /8/10| C:\Programme\Stueber Systems\Magellan 7  |
|Windows Server 2008 | C:\Program Files (x86)\Stueber Systems\Magellan 7  |
|Windows 8 | C:\Programme\Stueber Systems\Magellan 7  |
|Windows 10 | C:\Program Files (x86)\Stueber Systems\Magellan 7  |

Allgemeine Einstellungs- und Lizenzdaten (z.B. Magellan.evm, Magellan.lic, Magellan.SiteInfo, Magellan.UserInfo):

Betriebssystem | Pfad
--------------------| -------------
Windows 7 /8/10| C:\ProgramData\Stueber Systems\Magellan 7
Windows Server 2008 | C:\ProgramData\Stueber Systems\Magellan 7
Windows 8 | C:\ProgramData\Stueber Systems\Magellan 7
Windows 10 | C:\ProgramData\Stueber Systems\Magellan 7

Datenordner (Vorlagen, Skripte, Importe, Dokumente, Berichte, Datenordner):

Betriebssystem | Pfad
--------------------| -------------
Windows 7 /8/10| C:\Users\Public\Documents\Stueber Systems\Magellan 7
Windows Server 2008 | C:\ProgramData\Documents\Stueber Systems\Magellan 7
Windows 8 | C:\Users\Public\Documents\Stueber Systems\Magellan 7
Windows 10 | C:\Users\Public\Documents\Stueber Systems\Magellan 7

Die Pfade sind exemplarisch für die deutschen Versionen der Betriebssysteme und können je nach Sprache und Ausgabe des Betriebssystems variieren.

### Arbeitsplatzinstallation

Im Unterschied zur Serverinstallation werden bei der Arbeitsplatzinstallation nur die Anwendungs-, Einstellungs- und Lizenzdaten installiert. Die dafür verwendeten standardmäßigen Ordner entsprechen jenen bei der Serverinstallation.

### Einzelplatzinstallation

Die Einzelplatzinstallation entspricht der Serverinstallation.

### Magellan starten

Nach Beenden des Setup Assistenten müssen Sie Magellan 7 starten. Es erscheint zunächst der Willkommen-Assistent.

1. Klicken Sie auf `Weiter`. Um Magellan starten zu können, müssen Sie Ihre Lizenzdaten für eine Vollversion oder eine Testlizenz eingeben.

2. Wählen Sie `Eine Testlizenz anfordern` und klicken Sie dann auf `Weiter`, wenn Sie noch keine Lizenzdaten besitzen. Die Lizenzdaten können Sie dann mit Hilfe des Assistenten per E-Mail direkt anfordern oder als Textdatei speichern, falls Sie keinen E-Mailzugang besitzen. Wenn Sie Ihre Lizenzdaten erhalten haben, wählen Sie `Meine Lizenzdaten eingeben` und klicken Sie dann auf `Weiter`.

3. Tragen Sie nun Ihre Lizenzierung ein. Sollten Sie mit Ihren Lizenzdaten auch eine Lizenzdatei erhalten haben, so können Sie diese alternativ über `Lizenz importieren` einlesen. Klicken Sie dann auf `Weiter`.

4. Wählen Sie hier Ihr Bundesland aus und klicken dann auf `Weiter`.

5. Sie müssen entscheiden, ob Sie mit einer entfernten oder einer lokalen Datenbank arbeiten möchten. Bei einer Server-/Einzelplatzinstallation stellen Sie `Lokale Datenbank` ein. Bei einer Arbeitsplatzinstallation wählen Sie `Entfernte Datenbank`.

#### Entfernte Datenbank

Bei der Auswahl `Entfernte Datenbank` werden Sie zur Eingabe des Servernamens und des Datenbank-Pfads aufgefordert.

Geben Sie unter `Server` den Servernamen bzw. die IP-Adresse Ihres Servers ein, auf dem sich die Magellan 7 Datenbank befindet. Im unteren Feld geben Sie den lokalen Serverpfad (aus Sicht des Servers) zur Magellan 7 Datenbank an.

Der standardmäßige Pfad zur Magellan 7 Datenbank lautet:

Betriebssystem | Pfad
--------------------| -------------
Windows 7 /8/10| C:\Users\Public\Documents\Stueber Systems\Magellan 7\Datenbank\Magellan7.fdb
Windows 2003 | C:\ProgramData\Documents\Stueber Systems\Magellan 7\Datenbank\Magellan7.fdb
Windows 2008 | C:\ProgramData\Documents\Stueber Systems\Magellan 7\ Datenbank\Magellan7.fdb

Die Pfade sind exemplarisch für die deutschen Versionen der Betriebssysteme und können je nach Sprache und Ausgabe des Betriebssystems variieren. Wenn Sie die Originaleinstellungen während der Installation beibehalten haben, trifft einer der oben gezeigten Datenbankpfade zu.

##### Lokale Datenbank

Direkt auf dem Server oder einem Einzelplatz entscheiden Sie sich bitte für `Lokale Datenbank`. Sie werden dann zur Eingabe des Datenbankpfads aufgefordert.
Der standardmäßige Pfad zur Magellan 7 Datenbank lautet:

Betriebssystem | Pfad
--------------------| -------------
Windows 7 /8/10| C:\Users\Public\Documents\Stueber Systems\Magellan 7\Datenbank\Magellan7.fdb
Windows Server 2003 | C:\ProgramData\Documents\Stueber Systems\Magellan 7\Datenbank\Magellan7.fdb
Windows Server 2008 | C:\ProgramData\Documents\Stueber Systems\Magellan 7\Datenbank\Magellan7.fdb

Die Pfade sind exemplarisch für die deutschen Versionen der Betriebssysteme und können je nach Sprache und Ausgabe des Betriebssystems variieren. Wenn Sie die Originaleinstellungen während der Installation beibehalten haben, trifft einer der bei-den oben gezeigten Beispielpfade zu.

Im folgenden Fenster werden die Verzeichnisse der Datenordner abgefragt. In der Regel sind die Vorgaben richtig. Hat man die Skripte, Berichte, Dokumente etc. aber an anderer Stelle (z.B. auf dem Server) gespeichert, kann man dies hier angeben.

!!! info "Hinweis"

    Wünschen Sie andere Pfade als die vorgegebenen, stellen Sie es bitte in diesem Assistentenfenster ein. Ein Serviceupdate nutzt immer nur die Pfade, die zum Zeitpunkt der Installation in diesem Fenster angelegt worden sind. Eine nachträgliche Änderung kann nur mit einer erneuten Installation erfolgen.

Bestätigen Sie mit `Weiter` und klicken Sie auf `Starten`, um den Willkommen-Assistenten abzuschließen und MAGELLAN erstmalig zu starten.
Geben Sie im Anmeldedialog bei Benutzer `sysdba` und als Kennwort `masterkey` ein.

#### Probleme bei der Installation

Bitte schauen Sie den Abschnitt ["Probleme bei der Installation?"](https://doc.magellan6.stueber.de/installation/probleme-bei-der-installation.html) an!

#### Mehrere Arbeitsplatzrechner einrichten: Die Paths-Datei

Beim Start von MAGELLAN werden Informationen aus Dateien gelesen. Diese Dateien werden an einem betriebssystemspezifischen Ort pro Installation erwartet oder MAGELLAN liest den Inhalt der Paths-Datei (``Magellan.paths``) aus.

Der Vorteil einer Paths-Datei ist, dass Sie mehreren Nutzern die identischen Einstellungen in einem Arbeitsschritt an einem zentralen Ort zur Verfügung stellen können. Beim Einrichten einer neuen Arbeitsplatzinstallation genügt es die Installation durchzuführen und die Magellan.paths im Programmverzeichnis abzulegen.

Folgende Dateien werden beim Programmstart gelesen:

Datei | Inhalt
--------------------| -------------
Magellan.lic | enthält die Lizenzierungsdaten
Magellan.opt | enthält die Magellan-Optionseinstellungen
MagInv.opt | enthält die Magellan-Haushalt&Inventar-Optionseinstellungen
MagBib.opt | enthält die Magellan-Bibliothek-Optionseinstellungen
Magellan.evm | enthält die Pfade zur Datenbank und den Datenordnern

Diese Dateien liegen je nach Betriebssystem an folgenden voreingestellten Speicherorten:

Betriebssystem | Pfad
--------------------| -------------
Windows 2000 | C:\Dokumente und Einstellungen\All Users\Anwendungsdaten\Stueber Systems\Magellan 7
Windows XP | C:\Dokumente und Einstellungen\All Users\Anwendungsdaten\Stueber Systems\Magellan 7
Windows Vista | C:\ProgramData\Stueber Systems\Magellan 7
Windows 7/8 | C:\ProgramData\Stueber Systems\Magellan 7
Windows Server 2008 | C:\ProgramData\Stueber Systems\Magellan 7

Möchten Sie abweichende Speicherorte für diese Dateien angeben, zum Beispiel damit alle Magellan-Arbeitsplatzinstallationen auf dieselben Dateien zugreifen, sind folgende Schritte nötig:

1. Richten Sie einen Arbeitsplatz vollständig ein, damit Sie von diesem Arbeitsplatz aus die ``Magellan.evm``, die ``Magellan.lic`` und die ``Magellan.opt`` kopieren können.

2. Wählen Sie einen Speicherort für die Konfigurationsdateien aus. Die Dateien können in einem gemeinsamen Verzeichnis liegen oder Sie wählen für ``Magellan.evm``, ``Magellan.lic`` und die Optionsdateien (``Magellan.opt``, ``MagInv.opt``, ``Mag-Bib.opt``) drei getrennte Verzeichnisse und speichern dort die Dateien.

3. Erstellen Sie mit einem Texteditor eine neue Textdatei und kopieren den nachfolgenden Text in diese Datei. Passen Sie die Pfade bitte auf Ihre angelegten Verzeichnisse an, diese können sich lokal auf dem Rechner oder in Ihrem Netzwerk befinden.

Beispiel:

``` xml
<?xml version=`1.0` encoding=`UTF-8` standalone=`yes`?>
<Preferences>
<Paths>
<Entry Name=`MagellanEnvironmentFolder` Value=`D:\Mein Verzeichnis`/>
<Entry Name=`MagellanOptionsFolder` Value=`D:\Mein Verzeichnis`/>
<Entry Name=`MagellanLicenseFolder` Value=`D:\Mein Verzeichnis`/>
</Paths>
</Preferences>
```

Weiter geht's:

1. Speichern Sie diese Textdatei und benennen die Datei anschließend in `Magellan.paths` um.

2. Legen Sie diese Datei pro Arbeitsplatzinstallation im Programmverzeichnis ab. Beim Programmstart von MAGELLAN wird geprüft, ob sich eine Datei mit diesem Namen im Programmverzeichnis befindet und gegebenenfalls ausgelesen.

Über Neuerungen im Programm informieren wir im Abschnitt [Was ist neu?](http://doc.magellan6.stueber.de/changelog.html)

#### Lizenz erfassen

Die MAGELLAN Lizenz erfassen Sie üblicherweise beim Erststart von MAGELLAN im Willkommen-Assistenten. Hier lesen Sie nach, wie Sie die Lizenz nachträglich anpassen können, wenn Sie z.B. weitere Module freischalten möchten.

Es stehen Ihnen zwei Möglichkeiten der Lizenzerfassung zur Verfügung:

* Lizenzdaten von Hand eingeben
* Lizenzdaten importieren

##### Lizenzdaten von Hand eingeben

Um Ihre Lizenzdaten von Hand einzugeben, gehen Sie bitte folgendermaßen vor

1. Starten Sie MAGELLAN und führen Sie den Menüpunkt `Hilfe > Lizenz` aus.
2. Betätigen Sie im erscheinenden Dialogfenster `Lizenz` die Schaltfläche `Neue Lizenz`.
3. Tragen Sie im erscheinenden Dialogfenster `Lizenz ändern` Ihre Lizenzdaten ein. Diese umfassen den Namen, den Standort und den Schlüssel des Lizenznehmers.
4. Bestätigen Sie Ihre Eingaben abschließend mit `OK`.

Im Dialogfenster `Lizenz` werden anschließend neue Module bei bei den aktiven Modulen angezeigt und steht Ihnen nun fortan auf Ihrem Rechner zur Verfügung.

##### Lizenzdaten importieren

Alternativ können Sie Ihre Lizenzdatei auch importieren. Eine Lizenzdatei erhalten Sie entweder von STÜBER SYSTEMS als Anhang per E-Mail zugeschickt oder sie wird von MAGELLAN automatisch bei der Eingabe Ihrer Lizenzdaten erzeugt. Wenn z.B. an einem anderen Rechner Ihrer Schule bereits eine ausreichende Lizenzierung vorliegt, können Sie einfach die Lizenzdatei dieses Rechners importieren. Die erzeugte bzw. importierte Lizenzdatei wird unter dem Namen `Magellan.lic` standardmäßig in folgenden Windows-Verzeichnissen abgelegt:

Betriebssystem | Pfad
-------------- | ----
Windows Vista | `C:\ProgramData\Stueber Software\Magellan 7`
Windows XP | `C:\Dokumente und Einstellungen\All Users\Anwendungsdaten\Stueber Software\Magellan 7`
Windows 2000 | `C:\Dokumente und Einstellungen\All Users\Anwendungsdaten\Stueber Software\Magellan 7`

Um eine `Magellan.lic`-Datei zu importieren, führen Sie bitte folgende Schritte aus:

1. Öffnen Sie das Basismodul und führen Sie den Menüpunkt ```Hilfe|Lizenz``` aus.
2. Betätigen Sie im erscheinenden Dialogfenster `Lizenz` die Schaltfläche ```Lizenzdatei importieren```.
3. Markieren Sie im Windows-Explorer des erscheinenden Dialogfensters die gewünschte Lizenzdatei
4. Bestätigen Sie Ihre Auswahl mit ```Öffnen```.

Die Lizenzdaten der importierten Datei werden nun im Dialogfenster `Lizenz` angezeigt. Die freigeschalteten Module stehen nun auf Ihrem Rechner zur Verfügung.

## Deinstallation

Die Deinstallation von MAGELLAN starten Sie über den entsprechenden Aufruf unter ```Systemsteuerung > Programme und Funktionen``` oder indem Sie das Installationspaket erneut starten.

Bei der Deinstallation bleiben folgende Bestandteile erhalten:

* Ihre MAGELLAN-Datenbank
* Ihre MAGELLAN-DWH-Datenbank
* alle von Ihnen umbenannten Skripte und Berichte
* alle nicht von Ihnen umbenannten, aber an einen anderen Ort verschobenen Bestandteile
* die Lizenzdatei, die Optionsdateien, die EVM-Datei

## Updates

Wir veröffentlichen neue Funktionen, neue Berichte oder Skripte usw. per Serviceupdates. Diese Updates müssen auf den Rechner in Ihrem Netzwerk eingespielt werden. Nachstehend werden die Schritte dazu beschrieben.

### Update-Planung: Wird die Datenstruktur angepasst oder nicht

Das ist der erste Punkt, der vor der Planung der Updates geprüft werden sollte. Wird nach dem Update die Datenstruktur um neue Felder oder Tabellen erweitert, müssen vorübergehend alle Magellan-Nutzer von der Datenbank abgemeldet werden.

Im Abschnitt [Was ist neu?](http://doc.magellan6.stueber.de/changelog.html) auf unserer Webseite oder in unserem [Newsletter](http://www.stueber.de/newsletter.php) wird auf die `Datenstrukturerweiterung` pro veröffentlichter Version hingewiesen.

#### Updates ohne Datenstrukturerweiterung

Bitte aktualisieren Sie immer als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Sie können das aktuelle [msi-Paket](ftp://ftp.stueber.de/pub/bin/de/magellan/v6/magellan6.msi) von unserer Webseite herunterladen und direkt per Doppelklick starten oder dazu ein Tool zur Softwareverteilung nutzen.

##### Updates mit Datenstrukturerweiterung

Bitte aktualisieren Sie auch hier immer als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner!

Beim ersten Start von Magellan erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Sie müssen dazu wie folgt vorgehen:

1. Melden Sie sich als sysdba in Magellan an.
2. Alle anderen Benutzer müssen MAGELLAN verlassen haben!
3. Der Assistent zur Konvertierung erscheint, führen Sie zuerst die Sicherung Ihrer Datenbank und anschließend die die Konvertierung aus. Sollten Sie mehrere Strukturanpassungs-Updates übersprungen haben, werden diese der Reihe nach vom Assistenten durchgeführt. Schließen Sie MAGELLAN.
4. Rufen Sie den MAGELLAN-Administrator auf. Synchronisieren Sie die Zugriffsrechte der Benutzer (`Datenbankpflege > Datenbank prüfen`, Option: `Zugriffsrechte synchronisieren`).

!!! info "Hinweis"

    Falls es Probleme gibt, lesen Sie bitte [hier](http://doc.magellan6.stueber.de/installation/troubleshootingupdate.html) weiter!

#### Die Update-Infodatei

Jedes Installationspaket von MAGELLAN besitzt eine korrespondierende Update-Infodatei. Dies ist eine kleine XML-Datei, die es MAGELLAN ermöglicht, eine neuere Version automatisch zu erkennen, herunterzuladen und zu installieren. Update-Infodateien besitzen die Dateiendung `.UPDATEINFO`.

Die Update-Infodateien für MAGELLAN finden Sie hier: [Update-Infodatei für MAGELLAN-Setup](http://magellan.stueber.de/download.php)

Sie können die MAGELLAN so anpassen, dass aktuelle Updates nicht von unseren Internetseiten, sondern von einem Netzwerkpfad Ihres Netzwerks bezogen werden.

#### Lokales Ablegen des Setups

Laden Sie dazu das Installationspaket von unseren Internetseiten herunter, und legen Sie dieses zentral in einem für jeden Nutzer erreichbaren Ordner des Netzwerks ab. Laden Sie anschließend die zur Verfügung stehende Update-Infodatei von unserer Internetseite und legen diese in den selben Ordner. Öffnen Sie die Datei mit einem einfachen Textbearbeitungsprogramm (z.B. Windows Notepad) und passen Sie den Pfad des Installationspaketes an, indem Sie den FTP-Pfad gegen Ihren Netzwerkpfad austauschen.

Ein Beispiel für eine Update-Infodatei:

``` xml
<?xml version=`1.0` encoding=`utf-8`?>
<UpdateInfo>
<UpdatePackage
Product=`Magellan6`
ProductVersion=`7.0.14`
SetupFileName=`magellan6.msi`
SetupURL=`ftp://ftp.stueber.de/pub/bin/de/magellan/v7/magellan7.msi`
SetupSize=`243156992` />
</UpdateInfo>
```

#### Anpassen der Clients

Damit MAGELLAN weiß, dass es nicht auf unseren Internetseiten sondern in Ihrem Netzwerk nach neuen Updates suchen soll, müssen Sie bei allen Clients in MAGELLAN unter `Datenbank > Optionen > Auto-Update` den Pfad zu Ihrer Update-Infodatei eintragen.

[Update-Infodatei für MAGELLAN-Setup](http://magellan.stueber.de/download.php)

#### Firebird aktualisieren

Der Assistent zum Datenstrukturanpassen prüft vor der Erweiterung der Datenstruktur um neue Felder, Tabellen usw. die ODS-Version (on disc struktur) Ihrer Datenbank.
Diese ODS-Version erhält Ihre Datenbank durch das Sichern und Wiederherstellen mit der jeweils von uns empfohlenen Firebird-Version.

Bitte prüfen Sie vorab welche Version von Firebird Sie aktuell einsetzen. Die Versionsnummer wird Ihnen auf Ihrem Serverrechner unter `Start > Systemsteuerung > Programme und Funktionen > Firebird` gezeigt.
Nachfolgend beschreiben wir die Schritte beim Aktualisieren von 2.5.1/2.5.2 oder, hier sind einige Schritte mehr zu erledigen, von 2.1 auf die aktuell empfohlene Version.

Über Neuerungen im Programm informieren wir im Abschnitt [Was ist neu?](http://doc.magellan6.stueber.de/changelog.html)

### Neue Datenbank einrichten

Bevor Sie mit Magellan in den Realbetrieb starten, hatten Sie das Programm sicher mit einer Beispieldatenbank zum Test installiert. Die nachfolgenden Schritte beschreiben, wie man von der Beispieldatenbank in den Echtbetrieb wechselt.

1. Verbindung zur leeren Datenbank einrichten
2. Schlüsselverzeichnisse einlesen
3. Postleitzahlverzeichnis importieren
4. Mandanten anpassen
5. Zeiträume anlegen

### Leere Datenbank

Bei der erstmaligen Installation werden im Datenbank-Verzeichnis zwei Datenbanken abgelegt. Eine leere Datenbank und eine mit Beispieldaten gefüllte Datenbank. Sie haben vermutlich bis jetzt die Verbindung zur Beispieldatenbank verwendet um das Programm mit Testdaten anzusehen. Sie können jetzt den Verweis unter `Datenbankverbindungen > Doppelklick auf Ihre Verbindung > Datenbank` von `Magellan7_Beispiel.fdb` auf `Magellan7.fdb` abändern, dann greift die Verbindung auf die leere Datenbank zu.

!!! info "Hinweis"

    Eine "frische" leere Datenbank können Sie sich unter dem Punkt `Datenbankpflege > Mandanten kopieren > von 6 nach 7 > MAGELLAN Datenbank kopieren` über das Wolkensymbol unten links in der Fensterecke laden.

![Leere Datenbank](/assets/images/04.png)

### Schlüsselverzeichnisse einlesen

Importieren Sie im MAGELLAN Administrator anschließend unter ```Datenaustausch > Schlüsselverzeichnisse importieren``` die Schlüsselverzeichnisse für Ihr Bundesland und Ihre Schulart ein.

![Importieren der Schlüsselverzeichnisse](/assets/images/import.schl.png)

### Postleitzahlverzeichnis importieren

Importieren Sie im MAGELLAN Administrator anschließend unter ```Datenaustausch > Postleitzahlverzeichnisse importieren``` die Postleitzahlen.

![Importieren der Postleitzahlen](/assets/images/plz.png)

### Mandanten anpassen

Starten Sie im Anschluss MAGELLAN und rufen die Ansicht ```Mandanten``` auf. Doppelklicken Sie auf die vorhandene Mandantenzeile und passen auf der Karte Daten 1 die Daten des Beispielmandanten an Ihre realen Daten an.

### Zeiträume anlegen

Öffnen Sie jetzt in MAGELLAN den Punkt `Extras > Schlüsselverzeichnisse > Zeiträume` und legen ein neues Schuljahr (zwie neuen Halbjahre) über die Schaltfläche ```Schuljahre anlegen...``` an.

![neues Schuljahr anlegen](/assets/images/05.png)

### Datenimport über das Magellan-Importformat

Wir bieten für verschiedene Schulverwaltungsprogramme Schnittstellen an um Daten nach MAGELLAN übernehmen zu können. In der Regel ist das Vorgehen so, dass ein Konvertierungsassistent aus der Datenbasis des Altprogrammes Daten in unser MAGELLAN-Importformat konvertiert und Sie in einem zweiten Schritt diese Daten (csv-Format) über den Punkt `Datenaustausch > Daten über MAGELLAN-Importformat importieren` einlesen.

Gibt es keine Schnittstelle zu dem bislang von Ihnen verwendeten Programm oder verwalten Sie Ihre Daten bisher in Access oder Excel, können Sie diese Daten auch auf unser MAGELLAN Importformat anpassen und in die Datenbank einlesen. Ausführlich informieren wir dazu im Dokument [MAGELLAN-Toolbox im Abschnitt MAGELLAN-Importformat](https://doc.magellan7-toolbox.stueber.de/importe/).

### Schlüsselverzeichnisse

Wir liefern pro Region importierbare Schlüsselverzeichnisdateien mit. Die Menge der gelieferten Dateien richtet sich nach den Verzeichnisse, die wir MAGELLAN-intern benötigen plus den Verzeichnissen, die wir zum Beispiel für statistische Auswertungen von Ämtern geliefert bekommen.

Da sich Schlüsselwerte inaktuell werden können, gibt es folgenden Ablauf beim Punkt ```Datenaustausch > Schlüsselverzeichnisse importieren```:

Nr.|Aktion
--|--
1.|Alle noch nie verwendeten Schlüssel werden in den Zielverzeichnissen der Datenbank gelöscht.
2.|Alle übrigen Schlüssel werden in der Datenbank mit einem älteren Datum versehen und damit als ungültig(graue Raute) markiert.
3.|Nun wird geprüft welche Schlüssel eingelesen werden sollen, entscheidend ist dabei lediglich der Wert in der Spalte Schlüssel:<br/>- Wird ein Schlüssel erkannt, wird nur das Gültig-Bis-Datum entfernt (Schlüssel ist wieder aktiv). Das gilt auch, wenn der Schlüsselwert mehrfach im Verzeichnis existiert.<br/>- Wird ein Schlüssel nicht im Verzeichnis erkannt, wird er eingelesen und aktiv gesetzt.

!!! info "Hinweis"

    Als Ergebnis haben Sie damit nur die korrekten Schlüssel als aktive Werte markiert, verkehrt, aber bereits verwendete Schlüssel bleiben in der Datenbank, werden aber als inaktiv gekennzeichnet.
    Sie können auch eigene Werte über den Punkt ```Datenaustausch > Schlüsselverzeichnisse importieren``` einlesen. Sie müssten dafür lediglich die Benennung und den Aufbau der Schlüsselverzeichnisdateien berücksichtigen. Bitte lesen Sie dazu das Kapitel `Eigene Schlüsselverzeichnisse importieren` im Administrationsteil des MAGELLAN Benutzerhandbuchs.

## Benutzerverwaltung

Folgende Rechte stehen Ihnen für Ihre Benutzer zur Verfügung:

Rechtegruppe| Rechte
--|--
Schulleitung 1|Zugriff auf alle Daten außer auf die Datenbankstruktur und die Benutzer-verwaltung
Schulleitung 2|Wie Schulleitung 1, aber mit der Einschränkung, keine Fächer oder No-ten der Schüler zu ändern
Sekretariat 1|Zugriff auf alle Daten außer auf die Datenbankstruktur und Benutzerver-waltung
Sekretariat 2|Wie Sekretariat 1 aber mit folgenden Einschränkungen: Darf nur Fächer der Schüler sehen (d.h. Schüler/Zeugnis/Leistungen + Schü-ler/Zeugnis/Details + Zeugnisbemerkungen/-Formulare nicht sichtbar)
Kollegium 1|Die Noten und Zeugnisdaten der Schüler, die unterrichtet werden, dürfen erfasst bzw. geändert werden. Ansonsten bestehen nur Leserechte. <br/>Wenn Lehrer Klassenleiter 1 oder 2 oder Tutor ist, darf er die o.g. Daten aller Schüler seiner Klasse verändern (auch wenn er diese nicht unterrich-tet). <br/>Das Menü `Lehrer` zeigt nur die eigenen Personaldaten an. <br/>Kollegiumsrechte müssen zugewiesen sein, damit man MyMagellan-Dateien bearbeiten kann. Welche Voraussetzungen hierfür des Weiteren gegeben sein müssen, erfahren Sie im Abschnitt `Das MyMagellan Center` unter `Voraussetzungen`.
Kollegium 2|Wie Kollegium 1, zusätzlich auch Laufbahndaten und Fehlzeiten des Schülers editierbar
Kollegium 3|Wie Kollegium 2, aber keine Zeugnisformulare der Schüler editierbar
Kollegium 4|Wie Kollegium 2, aber keine Zeugnisformulare und Zeugnisbemerkun-gen editierbar
Kollegium 5|Wie Kollegium 2, zusätzlich auch das Abiturmenü für alle Schüler editier-bar
Gast 1|Leserechte. Schreibzugriff ist nicht möglich. Das Menü `Lehrer` zeigt nur die eigenen Personaldaten
Gast 2|Leserechte. Schreibzugriff ist nicht möglich. Das Menü `Lehrer` zeigt die Personaldaten aller Lehrer an.
Statistik-Administrator| Wie Schulleitung 1, zusätzlich können die folgenden Punkte ausgeführt werden: im Administratormodul `Schlüsselverzeichnisse importieren`, `Mach-Export`, den Abgleich zwischen Magellan und daVinci, Starten des DWH-Explorers

## Sicherung und Datenbankpflege

Im MAGELLAN Administrator können Sie unter dem Punkt `Datenbankverbindugn > Backup` können Sie eine Sicherungskopie für Ihre Datenbank erstellen. 



!!! warning "Wichtig"

    Bitte denken Sie daran, dass hierbei nur die Datenbank selbst gesichert wird, keins der Verzeichnisse Skripte, Berichte, Dokumente, Vorlagen usw.

### Sicherungskopie erstellen

Die Datensicherung wird im in den Verbindungseinstellungen hinterlegtem Backup-Verzeichnis angelegt.

![Gewählte Ablagestelle für die Sicherungskopie](/assets/images/07.png)

Öffnen Sie den Punkt `Datenbankverbindungen` und markieren die Zeile der Verbindung, deren Datenbank Sie sichern möchten. Wählen Sie anschließend die Schaltfläche `Backup` im Menüband aus, alternativ können Sie die gewählte Verbindung im Backup-Fenster auch noch anpassen.
Melden Sie sich als sysdba mit dem entsprechenden Passwort an und klicken Sie auf `Starten`. 
Den Namen für die Sicherungskopie vergibt das Programm selbständig.

![Sicherung erstellen](/assets/images/08.png)


!!! warning "Wichtig"

    Das Verzeichnis muss bereits existieren und es kann aus Sicherheitsgründen nur eine Sicherung auf dem Rechner abgelegt werden, auf dem auch die Datenbank liegt. Den Sicherungsprozess selbst können Sie hingegen auch von Arbeitsstationen aus starten.

    Von der Sicherungskopie sind alle Dokumente, Word-Vorlagen und Berichte ausgenommen.

!!! info "Hinweis"

    Eine Sicherungskopie kann im laufenden Betrieb von Magellan durchgeführt werden.

### Sicherungskopie wiederherstellen

Öffnen Sie den Punkt `Datenbankverbindungen` und markieren die Zeile der Verbindung, deren Datenbank Sie eine Sicherung wiederherstellen möchten. Wählen Sie anschließend die Schaltfläche `Wiederherstellen` im Menüband aus, alternativ können Sie die gewählte Verbindung im Wiederherstellen-Fenster auch noch anpassen.
Die Verbindung wählen Sie an der Stelle nur aus, damit auf den Backup-Ordner, den Sie der Verbindung zugewiesen haben, zugegriffen haben.

Klicken Sie auf die in der Abbildung markierte Schaltfläche am Ende der Zeile `Sicherung`. Es öffnet sich das Verzeichnis mit Ihren Sicherungen, Sie wählen die wiederherzustellende Sicherung aus.

![Verzeichnis mit der wiederherzustellenden Sicherung wählen](/assets/images/06.png)

Tragen Sie die Anmeldedaten für den `sysdba` ein und klicken Sie auf `Starten`. Ein Dateiname wird vom Programm selbständig vergeben.
Es wird eine neue Datenbank aus Ihrer Backup-Datei erstellt, sie wird entsprechend des Names der Sicherung benannt und in dem Verzeichnis abgelegt, dass Sie in den Verbindungseinstellungen dafür eingestellt haben.

!!! warning "Wichtig"

    Die Sicherung überschreibt nicht Ihre Produktivdatenbank, um Versehen zu vermeiden. An der Stelle würde eine Fehlermeldung ausgegeben werden.

!!! info "Hinweis"

    Das Herstellen einer Sicherungskopie und anschließende Wiederherstellen dieser Sicherungskopie hat eine reparierende und zugleich komprimierende Funktion. Die wiederhergestellte Sicherungskopie ist stets kleiner als die Ausgangsdatenbank, da Lücken in der Datenbank beseitigt werden und so die Datenmenge `abgespeckt` wird. Wir empfehlen in Abständen die Realdatenbank mit einer wiederhergestellten Sicherung zu ersetzen. Bitte beachten Sie, dass beim Austausch der Datenbank immer der Firebird-Server gestoppt ist. Diesen Dienst können Sie stoppen und starten in der Systemsteuerung Ihres Servers im Aufruf Firebird Server Manager.

!!! danger "Achtung"

    Sie können mit Hilfe einer Batchdatei, die in Abständen vom Windows Taskplaner ausgeführt wird, die Sicherung erstellen lassen. Die notwendigen Schritte beschreiben wir  hier: [https://doc.magellan7.stueber.de/schulverwaltung/admin/sicherung.windows.task/](https://doc.magellan7.stueber.de/schulverwaltung/admin/sicherung.windows.task/)

## Erstellen von MyMagellan-Dateien mit dem MyMagellan-Center

Das MyMagellan-Center ist das zentrale Administrationswerkzeug zur dezentralen Noteneingabe über MyMagellan. Es dient der Verteilung der Daten pro MyMagellan-Teilnehmer in jeweils eine MyMagel-lan-Datei (Export aus Magellan) und dem späteren Einsammeln der vom MyMagellan-Teilnehmer modifizierten MyMagellan-Dateien (Import nach Magellan).
Im Rahmen der Installation von Magellan erfolgt auch die Installation des MyMagellan-Centers. Um das MyMagellan Center zu starten, gehen Sie wie folgt vor:

1. Klicken Sie auf Start, dann auf Programme und dann auf STÜBER SYSTEMS.
2. Klicken Sie auf MyMagellan Center 6.
3. Tippen Sie Ihre Kennung und Ihr Kennwort ein und bestätigen Sie mit OK (Wenn Sie Magellan neu installiert haben, dann tippen Sie unter Kennung `sysdba` und das Kennwort `masterkey` ein).
MyMagellan ist ein Programm zur dezentralen Notenerfassung für die Benutzer von Magellan. Es besteht aus zwei Programmenteilen:

Modul|Wofür?
--|--
MyMagellan-Center| Dient dem Administrator zum Erzeugen und späteren Einsammeln von jeweils einer MyMagellan-Datei pro MyMagellan-Teilnehmer. Diese MyMagellan-Datei enthält nur die für den Teilnehmer aufgrund seiner Benutzerrechte relevanten Daten auf Basis der Magellan-Datenbank.
MyMagellan| Dient dem MyMagellan-Teilnehmer zur Eingabe seiner Noten. Er verwendet dazu die vom Administrator zuvor erzeugte MyMagellan-Datei.

Im Unterschied zur zentralen Noteneingabe an der Schule über die Magellan-Clients kann so jeder Teilnehmer von MyMagellan seine Noten auf einem beliebigen PC eingeben. Er benötigt dazu lediglich die vom MyMagellan Center erzeugte MyMagellan-Datei und muss MyMagellan auf seinem PC installieren. Die MyMagellan-Datei dient somit dem Datenaustausch zwischen MyMagellan und der Magellan-Datenbank.

Für die Erstellung der Lehrerdateien müssen im MAGELLAN Administrator und in MAGELLAN selbst einige Punkte gegeben sein:

### Voraussetzungen in der Benutzerverwaltung des MAGELLAN Administrators

Voraussetzung|Bemerkung
--|--
Teilnehmer von MAGELLAN|Unterkarte MyMAGELLAN, hier muss `Teilnehmer` gewählt werden
Rechtegruppe|Der Benutzer benötigt mindestens die Rechtegruppe Kollegium 1
Passwort für die Mym-Datei|Optional: als Kennwort kann das MAGELLAN-Kennwort oder ein gesondertes MyMAGELLAN-Kennwort verwendet werden.
Pfad zur Erzeugung der Mym-Datei|Auf der Unterkarte MyMAGELLAN in der Benutzerverwaltung muss für jeden Kollegen ein Pfad und ein Dateiname hinterlegt werden. An dieser Stelle wird später vom MyMAGELLAN-Center die mym-Datei erzeugt.

#### Voraussetzungen in MAGELLAN

Voraussetzung|Bemerkung
--|--
Lehrerzuweisung|mym-Dateien können für drei Lehrerrollen befüllt werden:<br/>- Tutor (erhält alle Fachzeilen des Schülers, kann weitere Daten editieren)<br/>- Klassenleiter (erhält alle Fachzeilen des Schülers, kann weitere Daten editieren)<br/>- Fachlehrer (erhält gezielt Fachzeilen des Schülers, kann weitere Daten nicht editieren)<br/> Je nach Rolle muss der Kollege auch zugewiesen werden: <br/>- ```Schüler > Zeugnis >Details > Tutor```<br/>- ```Klasse > Zeiträume >Zeitraum > Klassenleiter```<br/>- ```Schüler > Zeugnis > Fächer > Spalte Lehrer```
Schülerfächer|```Schüler > Zeugnis > Fächer``` muss gefüllt sein

Eine ausführliche Anleitung finden Sie im Administrationsteil des das [MAGELLAN-Benutzerhandbuchs](http://doc.magellan6.stueber.de).
