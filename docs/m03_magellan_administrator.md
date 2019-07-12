# M03 - MAGELLAN Administrator


Diese Unterlagen fassen die in der Schulung MAGELLAN-Administrator behandelten Themen zusammen. Eine umfangreichere Dokumentation zu Magellan bietet Ihnen das [Benutzerhandbuch](http://doc.magellan7.stueber.de).

Hinweis | Bemerkung
--------------- | ---------
**Dauer:** | 6 x 45 min
**Inhalt:** | - Installation, Deinstallation, Updates<br/>- neue Datenbank einrichten<br/>- Datenimporte über das Magellan-Importformat<br/>- Schlüsselverzeichnisse <br/>- Benutzerverwaltung<br/>- Sicherung und Datenbankpflege<br/>- Erstellen von MyMagellan-Dateien mit dem MyMagellan-Center
**Zielgruppe:** | Schuladministratoren
**Ablauf**:|09:30 – 11:00 Uhr  <br/>11:15 – 12:45 Uhr<br/>13:30 - 14:15 Uhr 

## Installation

> #### primary::Hinweis
>
> Bitte beachten Sie die ausführliche Beschreibung der [Installation](https://doc.magellan7.stueber.de/installation/). 

#### Systemvoraussetzungen


MAGELLAN ist kompatibel mit folgenden Betriebssystemen:


* Windows XP / 2003 / Vista / 2008 / 7 / 8 / 10 (32-Bit)
* Windows 7 / 8 / 2008 / 2012 / 2016 (64-Bit)


Es werden folgende Office-Versionen für das Erstellen von Serienbriefen unterstützt:


* Office 2003 / 2007 / 2010 / 2013 / 2016 (ab Version 6.5)


MAGELLAN benötigt keine besonderen Hardware-Anforderungen, lediglich die Bildschirmauflösung sollte 1024 x 768 Bildpunkte nicht unterschreiten.


#### Erstinstallation von MAGELLAN 6


Dieser Abschnitt beschreibt die Installation von MAGELLAN 6 mit den einzelnen Installationsschritten und Installationsarten. Bitte beachten Sie die Systemvoraussetzungen.


* Installation von Firebird
* Installation von MAGELLAN
* Serverinstallation
* Arbeitsplatzinstallation
* Einzelplatzinstallation
* MAGELLAN 6 starten nach Neuinstallation


#### Installation von Firebird 2.5


Laden Sie bitte das Firebird-Installationspaket von [aus dem Downloadbereich unserer Webseiten](http://magellan.stueber.de/download.php). Starten Sie anschließend die Firebird Installation durch einen Doppelklick auf die Datei ``Firebird-2.5.5....Win32.exe``. Bitte übernehmen Sie im daraufhin startenden Installationsassistenten auf der Karte `Komponenten auswählen` die voreingestellten Optionen.


Auf der Karte `Zusätzliche Aufgaben auswählen` übernehmen Sie bitte die Optionen und aktivieren zusätzlich das Häkchen `Die Firebird Client-Bibliothek ins Systemverzeichnis kopieren`.


> #### primary::Wichtig
>
> Firebird sollte nur dem Rechner installiert werden, auf dem zukünftig die Datenbank gespeichert wird. Das kann Ihr Server sein oder auch ein netzwerkunabhängiger Rechner.
>
> Firebird nutzt für den Datenverkehr den Port 3050, mitunter ist dieser Port durch die Windows Firewall gesperrt. Richten Sie bitte eine Ausnahme (Eingehende und Ausgehende Regel) für diesen Port ein und versuchen es bitte erneut.


#### Installation von MAGELLAN 6


Laden Sie bitte das MAGELLAN-Installationspaket [aus dem Downloadbereich unserer Webseiten](http://magellan.stueber.de/download.php). Starten Sie anschließend die Installation per Doppelklick auf die Datei ``Magellan6.msi``.


Der Setup Assistent von MAGELLAN 6 wird gestartet und die Installationsdateien werden entpackt.


Wählen Sie die gewünschte Installationsart aus:




Auswahl|Was passiert?
---|---
*Server* |Der Datenbank-Server (Firebird) und alle weiteren Module werden auf einem Server installiert. Auf diesen befindet sich im Regelfall die MAGELLAN 6 Datenbank. Die einzelnen Arbeitsstationen, welche auf den Server zugreifen, werden mit der Art `Arbeitsplatz` installiert.
*Einzelplatz* |Der Datenbank-Server und alle weiteren Module werden auf einem Rechner installiert. Sie entspricht der Serverinstallation im Netz und wird daher über die gleiche Option ausgewählt.
*Arbeitsplatz* |Es wird ein Arbeitsplatz in Netzwerk installiert. Dazu werden nur die Anwendungsdaten und der Datenbank-Client installiert, jedoch nicht Datenbank, Berichte oder Skripte. Eine Arbeitsplatzinstallation setzt eine Serverinstallation voraus. Firebird darf auf diesem Arbeitsplatz nicht installiert sein.


Die weiteren Beschreibungen finden Sie in den nachfolgenden Abschnitten `Serverinstallation`, `Arbeitsplatzinstallation` und `Einzelplatzinstallation.


> #### primary::Wichtig
>
> Die Installation des Datenbankservers (Firebird) wird für die Installationsarten Server und Einzelplatz vorausgesetzt.
#### Serverinstallation


Nachdem Sie die Installationsart `Server bzw. Einzelplatz` gewählt haben, ist der Setup Assistent bereit, die Installation der Dateien vorzunehmen. Die Installation selbst muss direkt auf dem Server erfolgen.


1. Wählen Sie zunächst den Speicherort für die Programmdateien aus.
2. Wählen Sie den Speicherort für die Datenbank und klicken Sie auf `Weiter`.
3. Wählen Sie den Speicherort für die Datenordner (Berichte-, Dokumente-, Importe-, Skripte- und Vorlagenordner) und klicken Sie auf `Weiter`.
4. Klicken Sie nun auf `Installieren`, um mit der Installation zu beginnen.
5. Die Installation selbst kann einige Minuten in Anspruch nehmen. Klicken Sie zum Abschließen der Installation auf `Fertigstellen`.




#### Speicherorte der Anwendungsdaten, Allgemeinen Einstellungs- und Lizenzdateien und der Datenordner


Nach Abschluss der Installation befinden sich standardmäßig die Dateien in folgenden Ordnern auf dem Server:


Anwendungsdaten (z.B. Magellan.exe):


Betriebssystem | Pfad
--------------------| -------------
Windows Vista | C:\Program Files\Stueber Systems\Magellan 6
Windows XP | C:\Programme\Stueber Systems\Magellan 6
Windows 2000 | C:\Programme\Stueber Systems\Magellan 6
Windows 7 | C:\Programme\Stueber Systems\Magellan 6
Windows Server 2008 | C:\Program Files (x86)\Stueber Systems\Magellan 6\
Windows 8 | C:\Programme\Stueber Systems\Magellan 6
Windows 10 | C:\Program Files (x86)\Stueber Systems\Magellan 6\


Allgemeine Einstellungs- und Lizenzdaten (z.B. Magellan.evm, Magellan.lic, Magellan.SiteInfo, Magellan.UserInfo):


Betriebssystem | Pfad
--------------------| -------------
Windows Vista | C:\ProgramData\Stueber Software\Magellan 6
Windows XP | C:\Dokumente und Einstellungen\All Users\Anwendungsdaten\Stueber Software\Magellan 6
Windows 2000 | C:\Dokumente und Einstellungen\All Users\Anwendungsdaten\Stueber Software\Magellan 6
Windows 7 | C:\ProgramData\Stueber Software\Magellan 6
Windows Server 2008 | C:\ProgramData\Stueber Software\Magellan 6
Windows 8 | C:\ProgramData\Stueber Software\Magellan 6
Windows 10 | C:\ProgramData\Stueber Software\Magellan 6


Datenordner (Vorlagen, Skripte, Importe, Dokumente, Berichte, Datenordner):


Betriebssystem | Pfad
--------------------| -------------
Windows Vista | C:\Users\Public\Documents\Stueber Systems\Magellan 6
Windows XP | C:\Dokumente und Einstellungen\All Users\Anwendungsdaten\Stueber Systems\Magellan 6
Windows 2000 | C:\Dokumente und Einstellungen\All Users\Dokumente\Stueber Systems\Magellan 6
Windows 7 | C:\Users\Public\Documents\Stueber Systems\Magellan 6
Windows Server 2008 | C:\ProgramData\Documents\Stueber Systems\Magellan 6
Windows 8 | C:\Users\Public\Documents\Stueber Systems\Magellan 6
Windows 10 | C:\Users\Public\Documents\Stueber Systems\Magellan 6


Die Pfade sind exemplarisch für die deutschen Versionen der Betriebssysteme und können je nach Sprache und Ausgabe des Betriebssystems variieren.


#### Arbeitsplatzinstallation


Im Unterschied zur Serverinstallation werden bei der Arbeitsplatzinstallation nur die Anwendungs-, Einstellungs- und Lizenzdaten installiert. Die dafür verwendeten standardmäßigen Ordner entsprechen jenen bei der Serverinstallation.


#### Einzelplatzinstallation


Die Einzelplatzinstallation entspricht der Serverinstallation.


#### Magellan 6 starten nach Neuinstallation


Nach Beenden des Setup Assistenten müssen Sie MAGELLAN 6 starten. Es erscheint zunächst der Willkommen-Assistent.


1. Klicken Sie auf `Weiter`. Um Magellan starten zu können, müssen Sie Ihre Lizenzdaten für eine Vollversion oder eine Testlizenz eingeben.


2. Wählen Sie `Eine Testlizenz anfordern` und klicken Sie dann auf `Weiter`, wenn Sie noch keine Lizenzdaten besitzen. Die Lizenzdaten können Sie dann mit Hilfe des Assistenten per E-Mail direkt anfordern oder als Textdatei speichern, falls Sie keinen E-Mailzugang besitzen. Wenn Sie Ihre Lizenzdaten erhalten haben, wählen Sie `Meine Lizenzdaten eingeben` und klicken Sie dann auf `Weiter`.


3. Tragen Sie nun Ihre Lizenzierung ein. Sollten Sie mit Ihren Lizenzdaten auch eine Lizenzdatei erhalten haben, so können Sie diese alternativ über `Lizenz importieren` einlesen. Klicken Sie dann auf `Weiter`.


4. Wählen Sie hier Ihr Bundesland aus und klicken dann auf `Weiter`.


5. Sie müssen entscheiden, ob Sie mit einer entfernten oder einer lokalen Datenbank arbeiten möchten. Bei einer Server-/Einzelplatzinstallation stellen Sie `Lokale Datenbank` ein. Bei einer Arbeitsplatzinstallation wählen Sie `Entfernte Datenbank`.


##### Entfernte Datenbank


Bei der Auswahl `Entfernte Datenbank` werden Sie zur Eingabe des Servernamens und des Datenbank-Pfads aufgefordert.


Geben Sie unter `Server` den Servernamen bzw. die IP-Adresse Ihres Servers ein, auf dem sich die MAGELLAN 6 Datenbank befindet. Im unteren Feld geben Sie den lokalen Serverpfad (aus Sicht des Servers) zur MAGELLAN 6 Datenbank an.


Der standardmäßige Pfad zur MAGELLAN 6 Datenbank lautet:


Betriebssystem | Pfad
--------------------| -------------
Windows Vista | C:\Users\Public\Documents\Magellan 6\Datenbank\Magellan6.fdb
Windows XP | C:\Dokumente und Einstellungen\All Users\Anwendungsdaten\Stueber Software \Magellan 6\Datenbank\Magellan6.fdb
Windows 2000 | C:\Dokumente und Einstellungen\All Users\Dokumente\Stueber Software\Magellan 6\Datenbank\Magellan6.fdb
Windows 7 | C:\Users\Public\Documents\Stueber Software\Magellan 6\Datenbank\Magellan6.fdb
Windows 2003 | C:\ProgramData\Documents\Stueber Software\Magellan 6\Datenbank\Magellan6.fdb
Windows 2008 | C:\ProgramData\Documents\Stueber Software\Magellan 6\ Datenbank\Magellan6.fdb


Die Pfade sind exemplarisch für die deutschen Versionen der Betriebssysteme und können je nach Sprache und Ausgabe des Betriebssystems variieren. Wenn Sie die Originaleinstellungen während der Installation beibehalten haben, trifft einer der oben gezeigten Datenbankpfade zu.


##### Lokale Datenbank


Direkt auf dem Server oder einem Einzelplatz entscheiden Sie sich bitte für `Lokale Datenbank`. Sie werden dann zur Eingabe des Datenbankpfads aufgefordert.
Der standardmäßige Pfad zur MAGELLAN 6 Datenbank lautet:


Betriebssystem | Pfad
--------------------| -------------
Windows Vista | C:\Users\Public\Documents\Magellan 6\Datenbank\Magellan6.fdb
Windows XP | C:\Dokumente und Einstellungen\All Users\Anwendungsdaten\Stueber Software\Magellan 6\Datenbank\Magellan6.fdb
Windows 2000 | C:\Dokumente und Einstellungen\All Users\Dokumente\Stueber Software\Magellan 6\Datenbank\Magellan6.fdb
Windows 7 | C:\Users\Public\Documents\Stueber Software\Magellan 6\Datenbank\Magellan6.fdb
Windows Server 2003 | C:\ProgramData\Documents\Stueber Software\Magellan 6\Datenbank\Magellan6.fdb
Windows Server 2008 | C:\ProgramData\Documents\Stueber Software\Magellan 6\Datenbank\Magellan6.fdb


Die Pfade sind exemplarisch für die deutschen Versionen der Betriebssysteme und können je nach Sprache und Ausgabe des Betriebssystems variieren. Wenn Sie die Originaleinstellungen während der Installation beibehalten haben, trifft einer der bei-den oben gezeigten Beispielpfade zu.


Im folgenden Fenster werden die Verzeichnisse der Datenordner abgefragt. In der Regel sind die Vorgaben richtig. Hat man die Skripte, Berichte, Dokumente etc. aber an anderer Stelle (z.B. auf dem Server) gespeichert, kann man dies hier angeben.


> #### danger::Achtung!
>
>  Wünschen Sie andere Pfade als die vorgegebenen, stellen Sie es bitte in diesem Assistentenfenster ein. Ein Serviceupdate nutzt immer nur die Pfade, die zum Zeitpunkt der Installation in diesem Fenster angelegt worden sind. Eine nachträgliche Änderung kann nur mit einer erneuten Installation erfolgen.


Bestätigen Sie mit `Weiter` und klicken Sie auf `Starten`, um den Willkommen-Assistenten abzuschließen und MAGELLAN erstmalig zu starten.
Geben Sie im Anmeldedialog bei Benutzer `sysdba` und als Kennwort `masterkey` ein.

#### Probleme bei der Installation? 

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
Windows 2000 | C:\Dokumente und Einstellungen\All Users\Anwendungsdaten\Stueber Software\Magellan 6
Windows XP | C:\Dokumente und Einstellungen\All Users\Anwendungsdaten\Stueber Software\Magellan 6
Windows Vista | C:\ProgramData\Stueber Software\Magellan 6
Windows 7/8 | C:\ProgramData\Stueber Software\Magellan 6
Windows Server 2008 | C:\ProgramData\Stueber Software\Magellan 6


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
Windows Vista | `C:\ProgramData\Stueber Software\Magellan 6`
Windows XP | `C:\Dokumente und Einstellungen\All Users\Anwendungsdaten\Stueber Software\Magellan 6`
Windows 2000 | `C:\Dokumente und Einstellungen\All Users\Anwendungsdaten\Stueber Software\Magellan 6`


Um eine `Magellan.lic`-Datei zu importieren, führen Sie bitte folgende Schritte aus:


1. Öffnen Sie das Basismodul und führen Sie den Menüpunkt ```Hilfe|Lizenz``` aus.


2. Betätigen Sie im erscheinenden Dialogfenster `Lizenz` die Schaltfläche ```Lizenzdatei importieren```.


3. Markieren Sie im Windows-Explorer des erscheinenden Dialogfensters die gewünschte Lizenzdatei.


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


#### Update-Planung: Wird die Datenstruktur angepasst oder nicht?


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


> #### primary::Hinweis
>
> Falls es Probleme gibt, lesen Sie bitte [hier](http://doc.magellan6.stueber.de/installation/troubleshootingupdate.html) weiter!


#### Probleme beim Einspielen der Service-Updates?


In den nachfolgenden Punkte beschreiben wir die Lösungen zu Problemen, die bei Updates auftreten können.


##### Datenbanksicherung kann nicht erstellt werden


Die Sicherung der Datenbank kann nur auf dem selben Rechner erstellt werden, auf dem auch die Datenbank selbst gespeichert ist. Versuchen Sie die Sicherung auf einem anderen Rechner oder über ein Netzlaufwerk erstellen zu lassen, stoppt der Assistent mit nachfolgender Meldung.
Bitte wählen Sie einen lokales Verzeichnis, wir empfehlen das Verzeichnis `Backup` in Ihrem Datenbankverzeichnis und einen Dateinamen, der das Tagesdatum enthält.


Beispiel die Benennung: 2016-04-23.fbk


![Datensicherung](images/sicherung nicht lokal speichern.jpg)


##### Die Magellan-Datenbank-ODS-Version ist nicht aktuell


Der Assistent prüft die ODS-Version (On-Disc-Structure) der Datenbank, um das Strukturupdate korrekt ausführen zu können. Ihre Datenbank sollte für die Anpassung bestimmte Befehle `kennen`. Durch das Sichern und anschließende Wiederherstellen erhöht sich die ODS-Version , d.h. die Datenbank `lernt` neue Befehle.


Folgende Schritte sind nötig:


1. Firebird aktualisieren
2. Sichern und Wiederherstellen der Datenbank im MAGELLAN ADMINISTRATOR > Datensicherung
3. Firebird stoppen
4. wiederhergestellte Datenbank gegen Realdatenbank tauschen
5. Firebird starten
6. MAGELLAN starten Datenstruktur anpassen
7. MAGELLAN ADMINISTRATOR starten und `Datenbankpflege > Zugriffsrechte synchronisieren` ausführen.


Prüfen Sie bitte auf Ihrem Serverrechner in der Systemsteuerung im `Firebird-Server-Manager` oder unter dem Punkt `Programme und Funktionen > Firebird` welche Version von Firebird Sie einsetzen, aktuell empfehlen wir die Version 2.5.5.


Wenn Sie diese Meldung erhalten, laden Sie über den Link unten links im Meldungsfenster die aktuelle Firebird-Version herunter. Stoppen Sie dann die aktuelle Firebird-Installation auf dem Serverrechner unter ```Systemsteuerung > Klassische Ansicht > Firebird-Server-Manager``` und schließen das Firebird-Fenster wieder.


Falls Sie den Aufruf in der Systemsteuerung nicht finden können, rufen Sie stattdessen den Punkt ```Systemsteuerung > Verwaltung > Dienste > Firebird-Server ```per Doppelklick auf stoppen den Dienst hier.


Starten Sie anschließend die Installation von Firebird per Doppelklick auf das Installationspaket und folgen dem Assistenten. Starten Sie anschließend den Firebird-Dienst wieder in der Systemsteuerung. Wenn Sie diese Version bereits einsetzen, dann fehlen noch die folgenden Schritte:


1. Melden Sie sich auf dem Serverrechner als sysdba am Magellan-Administrator an. Es wird erkannt, dass die Datenbank nicht in der aktuellen Version vorliegt, daher wird der Administrator nur mit dem Punkt Datenbanksicherung geöffnet.


2. Wählen Sie den Punkt ```Datensicherung > Sicherungskopie```, geben einen Pfad und einen Datennamen an. 
Beispiel: ```C:\Users\Public\Documents\Stueber Systems\Magellan 6\Datenbank\Backup\2016-03-24.fbk``` Starten Sie die Sicherung!


3. Im Anschluss stellen Sie die Datensicherung wieder her, die `Echtdatenbank` kann dabei nicht überschrieben werden.


4. Stoppen den Firebird-Dienst (Systemsteuerung|Firebird Server Manager).


5. Tauschen die Echtdatenbank gegen die wiederhergestellte Datenbank aus und starten den Firebird-Dienst wieder.

> #### primary::Hinweis
> Den Pfad zur Echtdatenbank auf Ihrem Serverrechner finden Sie unter ```MAGELLAN ADMINISTRATOR > Server-Verwaltung > Verbindungen verwalten > Starten > Verbindung markieren > Bearbeiten > Unterkarte Datenordner```.

6. Starten Sie MAGELLAN erneut als sysdba und führen Sie die Datenstrukturerweiterung aus.



#### Andere Benutzer sind noch angemeldet


Für die Datenstrukturanpassung darf kein Nutzer außer dem sysdba, der die Anpassung durchführt, angemeldet sein. Wenn Sie nicht wissen, wer in Ihrem Netzwerk noch ein Magellan-Modul(Schulverwaltung, Bibliothek, Haushalt&Inventar u.a) gestartet hat, können Sie den Firebird-Dienst stoppen und erneut starten. Öffnen Sie dazu auf Ihrem Server-Rechner in der Systemsteuerung den Punkt Firebird-Server-Manager, stoppen den Dienst und starten ihn erneut.


![](images/fb-server-control.jpg)


Fehlt Ihnen der Aufruf in der Systemsteuerung? Sie können den Dienst auch unter `Systemsteuerung > Verwaltung > Dienste > Firebird-Server` finden.


#### Trotz Update fehlen Skripte oder andere aktuelle Daten


Sie spielen das Update ein und dennoch fehlen Skripte für die Strukturanpassung oder zum Beispiel das in der LiesMich-Datei angekündigte neue Zeugnis?


Fünf Möglichkeiten können hinter diesem Problem stecken:


Nr | Ursache
-- | -------
1. | dem Server fehlt das Update und damit auch zum Beispiel die Strukturanpassungsskripte
2. | der Server hat das Update erhalten, aber das Update konnte die Anpassungsskripte nicht ablegen
3. | die Pfade zum Skripteverzeichnis auf dem Server fehlen
4. | die Pfade zum Skripteverzeichnis auf dem Server sind verkehrt
5. | Sie haben eine Einzelplatzinstallation und haben Ihr Betriebssystem auf Windows 10 aktualisiert


**Zu 1.: **


Bitte immer als erstes den Serverrechner aktualisieren, da dieser Rechner der einzige im Netzwerk ist, der die gemeinsam genutzten Programmkomponenten, wie zum Beispiel die Skripte hat und für die Clientinstallationen zur Verfügung stellt.


**Zu 2.:**


Sollten nach dem Update die Skripte u.a. dennoch nicht aktuell sein, kann es damit zusammenhängen, dass nach der ursprünglichen Serverinstallation die Pfade nachträglich verschoben wurden. Der bei der Installation und bei den Updates verwendete Windows Installer `möchte` die Dateien am ursprünglichen Speicherort aktualisieren. Sollte dieser nicht mehr bestehen, müsste erneut installiert werden und gleich auf die gewünschten Pfade verwiesen werden.


**Zu 3. und 4.:**


Eventuell wurde bei der Installation kein oder nicht der korrekte Pfad zu dem Skripteordner erfasst. Bitte rufen Sie das Anmeldefenster des Administrators auf und wählen die folgende Einstellung:


![](images/admin_ohne_anmeldung.jpg)


Anschließend rufen Sie im Administrator den Punkt `Server-Verwaltung > Verbindungen verwalten > Starten > Verbindung markieren > Bearbeiten > Unterkarte Datenordner` auf. Steht dort der Pfad zum Ordner Skripte? Wenn nicht tragen Sie ihn bitte nach.
Die Datenordner liegen je nach Betriebssystem bei unverändert übernommenen Installationspfaden an den nachfolgenden Stellen:
(Pfad bitte jeweils um den Namen des Verzeichnisses ergänzen: Berichte, Skripte, Vorlagen, Importe, Dokumente, Datenbank) finden Sie unter:


Betriebssystem | Standardpfad
------------------- | ------------
Vista | C:\Users\Public\Documents\Magellan 6
XP | C:\Dokumente und Einstellungen\All Users\Anwendungsdaten\Stueber S...\Magellan 6
Windows 2000 | C:\Dokumente und Einstellungen\All Users\Dokumente\Stueber S...\Magellan 6
Windows 7 | C:\Users\Public\Documents\Stueber S...\Magellan 6
Windows Server 2008 | C:\Users\Public\Documents\Stueber S...\Magellan 6


**zu 5.:**
Wenn Sie Ihren Rechner mit einer bestehenden MAGELLAN-Installationauf Windows 10 aktualisieren, kann es passieren, dass beim Folgeupdate von Magellan die Datenordner vom Windows Installer nicht gefunden werden und keine neuen Bestandteile wie Skripte, Berichte usw abgelegt werden.
Das betrifft keine Clientinstallationen die auf Datenordner auf dem Serverrechner nutzen, sondern nur Server-/Einzelplatzinstallationen. Bitte deinstallieren Sie MAGELLAN und installieren Sie es neu!


#### Die Update-Infodatei


Jedes Installationspaket von MAGELLAN besitzt eine korrespondierende Update-Infodatei. Dies ist eine kleine XML-Datei, die es MAGELLAN ermöglicht, eine neuere Version automatisch zu erkennen, herunterzuladen und zu installieren. Update-Infodateien besitzen die Dateiendung `.UPDATEINFO`.


Die Update-Infodateien für MAGELLAN finden Sie hier:


* [Update-Infodatei für MAGELLAN-Setup](http://magellan.stueber.de/download.php)


Sie können die MAGELLAN so anpassen, dass aktuelle Updates nicht von unseren Internetseiten, sondern von einem Netzwerkpfad Ihres Netzwerks bezogen werden.


#### Lokales Ablegen des Setups


Laden Sie dazu das Installationspaket von unseren Internetseiten herunter, und legen Sie dieses zentral in einem für jeden Nutzer erreichbaren Ordner des Netzwerks ab. Laden Sie anschließend die zur Verfügung stehende Update-Infodatei von unserer Internetseite und legen diese in den selben Ordner. Öffnen Sie die Datei mit einem einfachen Textbearbeitungsprogramm (z.B. Windows Notepad) und passen Sie den Pfad des Installationspaketes an, indem Sie den FTP-Pfad gegen Ihren Netzwerkpfad austauschen.


Ein Beispiel für eine Update-Infodatei:


``` xml
<?xml version=`1.0` encoding=`utf-8`?>
<UpdateInfo>
<UpdatePackage
Product=`Magellan6`
ProductVersion=`6.0.174`
SetupFileName=`magellan6.msi`
SetupURL=`ftp://ftp.stueber.de/pub/bin/de/magellan/v6/magellan6.msi`
SetupSize=`243156992` />
</UpdateInfo>
```

#### Anpassen der Clients


Damit MAGELLAN weiß, dass es nicht auf unseren Internetseiten sondern in Ihrem Netzwerk nach neuen Updates suchen soll, müssen Sie bei allen Clients unter `Extras > Optionen > Auto-Update` den Pfad zu Ihrer Update-Infodatei eintragen.


[Update-Infodatei für MAGELLAN-Setup](http://magellan.stueber.de/download.php)


#### Firebird aktualisieren


Der Assistent zum Datenstrukturanpassen prüft vor der Erweiterung der Datenstruktur um neue Felder, Tabellen usw. die ODS-Version (on disc struktur) Ihrer Datenbank.
Diese ODS-Version erhält Ihre Datenbank durch das Sichern und Wiederherstellen mit der jeweils von uns empfohlenen Firebird-Version.


Bitte prüfen Sie vorab welche Version von Firebird Sie aktuell einsetzen. Die Versionsnummer wird Ihnen auf Ihrem Serverrechner unter `Start > Systemsteuerung > Programme und Funktionen > Firebird` gezeigt.
Nachfolgend beschreiben wir die Schritte beim Aktualisieren von 2.5.1/2.5.2 oder, hier sind einige Schritte mehr zu erledigen, von 2.1 auf die aktuell empfohlene Version.


Über Neuerungen im Programm informieren wir im Abschnitt [Was ist neu?](http://doc.magellan6.stueber.de/changelog.html)


## Neue Datenbank einrichten


Bevor Sie mit Magellan in den Realbetrieb starten, hatten Sie das Programm sicher mit einer Beispieldatenbank zum Test installiert. Die nachfolgenden Schritte beschreiben, wie man von der Beispieldatenbank in den Echtbetrieb wechselt.


1. Datenbankkopie sichern (Firebirdserver stoppen!)
2. Datenbank leeren und Generatoren synchronisieren
3. Schlüsselverzeichnisse einlesen
4. Postleitzahlverzeichnis importieren
5. Mandanten anpassen
6. Zeiträume anlegen


##### Datenbankkopie sichern


Dieser Schritt ist optional, aber vielleicht möchten Sie eine Kopie der Beispieldatenbank erhalten, um mit einer zweite Datenbankanbindung auf diese Datenbank zum Test zu verweisen?
Stoppen Sie vor dem Kopieren bitte den Firebirdserver, entweder unter Verwaltung > Dienste oder über das Control in der Systemsteuerung. Kopieren Sie die Datenbank, vergeben für die Kopie einen eindeutigen Namen, zum Beispiel `Beispiel.fdb`, starten den Firebirdserver wieder und richten im Magellan Administrator eine zweite Verbindung ein, die auf diese Datenbank verweist. Fertig!


#### Datenbank leeren und Generatoren synchronisieren
Melden Sie sich als sysdba am Magellan-Administrator an und wählen den Punkt Datenbankpflege > Datenbankinhalt löschen.
Bitte leeren Sie auch das Postleitzahlverzeichnis und die Schlüsselverzeichnisse. Im Anschluss an den Assistenten startet automatisch die Aktion `Generatoren synchronisieren`. Hierbei werden in allen Tabellen die ID-Generatoren zurückgesetzt, damit zum Beispiel der erste neu angelegte Schüler auch die ID 1 erhält.



![Leeren des Datenbankinhaltes](/images/db.leeren.png)


#### Schlüsselverzeichnisse einlesen


Importieren Sie im MAGELLAN Administrator anschließend unter ```Datenimporte > Schlüsselverzeichnisse importieren``` die Schlüsselverzeichnisse für Ihr Bundesland und Ihre Schulart ein.


![Importieren der Schlüsselverzeichnisse](images/import.schl.png)


#### Postleitzahlverzeichnis importieren
Importieren Sie im MAGELLAN Administrator anschließend unter ```Datenimporte > Postleitzahlverzeichnisse importieren``` die Postleitzahlen.


![Importieren der Postleitzahlen](images/plz.png)


#### Mandanten anpassen


Starten Sie im Anschluss MAGELLAN und rufen die Ansicht ```Mandanten``` auf. Doppelklicken Sie auf die vorhandene Mandantenzeile und passen auf der Karte Daten 1 die Daten des Beispielmandanten an Ihre realen Daten an.


#### Zeiträume anlegen
Öffnen Sie jetzt in MAGELLAN den Punkt Verzeichnisse > Zeiträume und legen ein neues Schuljahr (zwie neuen Halbjahre) über die Schaltfläche ```Schuljahre anlegen...``` an.


![neues Schuljahr anlegen](images/zr.png)


## Datenimporte über das Magellan-Importformat


Wir bieten für verschiedene Schulverwaltungsprogramme Schnittstellen an um Daten nach MAGELLAN übernehmen zu können. In der Regel ist das Vorgehen so, dass ein Konvertierungsassistent aus der Datenbasis des Altprogrammes Daten in unser MAGELLAN-Importformat konvertiert und Sie in einem zweiten Schritt diese Daten (csv-Format) über den Punkt ```Datenimport > Daten über MAGELLAN-Importformat``` importieren einlesen.


Gibt es keine Schnittstelle zu dem bislang von Ihnen verwendeten Programm oder verwalten Sie Ihre Daten bisher in Access oder Excel, können Sie diese Daten auch auf unser MAGELLAN Importformat anpassen und in die Datenbank einlesen.
Ausführlich informieren wir dazu im Dokument MAGELLAN-Import.


## Schlüsselverzeichnisse


Wir liefern pro Region importierbare Schlüsselverzeichnisdateien mit. Die Menge der gelieferten Dateien richtet sich nach den Verzeichnisse, die wir MAGELLAN-intern benötigen plus den Verzeichnissen, die wir zum Beispiel für statistische Auswertungen von Ämtern geliefert bekommen.


Da sich Schlüsselwerte inaktuell werden können, gibt es folgenden Ablauf beim Punkt ```Datenimport > Schlüsselverzeichnisse importieren ```:


Nr.|Aktion
--|--
1.|Alle noch nie verwendeten Schlüssel werden in den Zielverzeichnissen der Datenbank gelöscht.
2.|Alle übrigen Schlüssel werden in der Datenbank mit einem älteren Datum versehen und damit als ungültig(graue Raute) markiert.
3.|Nun wird geprüft welche Schlüssel eingelesen werden sollen, entscheidend ist dabei lediglich der Wert in der Spalte Schlüssel:<br/>- Wird ein Schlüssel erkannt, wird nur das Gültig-Bis-Datum entfernt (Schlüssel ist wieder aktiv). Das gilt auch, wenn der Schlüsselwert mehrfach im Verzeichnis existiert.<br/>- Wird ein Schlüssel nicht im Verzeichnis erkannt, wird er eingelesen und aktiv gesetzt.


> #### primary::Hinweis
>
> Als Ergebnis haben Sie damit nur die korrekten Schlüssel als aktive Werte markiert, verkehrt, aber bereits verwendete Schlüssel bleiben in der Datenbank, werden aber als inaktiv gekennzeichnet.
>
> Sie können auch eigene Werte über den Punkt ```Datenimport > Schlüsselverzeichnisse importieren ``` einlesen. Sie müssten dafür lediglich die Benennung und den Aufbau der Schlüsselverzeichnisdateien berücksichtigen. Bitte lesen Sie dazu das Kapitel `Eigene Schlüsselverzeichnisse importieren` im Administrationsteil des MAGELLAN Benutzerhandbuchs.


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


Im MAGELLAN Administrator kommen Sie unter dem Punkt `Datensicherung` zu den Datensicherungsmöglichkeiten für Ihre Datenbank. Bitte denken Sie daran, dass hierbei nur die Datenbank selbst gesichert wird, keins der Verzeichnisse Skripte, Berichte, Dokumente, Vorlagen usw.


#### Sicherungskopie erstellen


Klicken Sie auf dem Serverrechner auf Sicherungskopie erstellen, um eine Sicherung der Magellan-Datenbank durchführen zu können. Im Fenster `Sicherungskopie erstellen` müssen Sie zunächst im Auswahlfeld `Welche Datenbank soll überprüft werden?` einstellen, ob die Magellan-Datenbank oder das Magellan Datawarehouse gesichert werden soll. `Sicherungskopie erstellen` bezieht sich jeweils auf die Datenbank, an der Sie sich angemeldet haben.


Wenn Sie die gewünschte Datenbank ausgewählt haben, klicken Sie bitte im Feld Dateiname der Sicherungskopie auf das kleine Lupensymbol. Es wird daraufhin ein Explorer geöffnet, in dem Sie den Speicherort der zu erstellenden Sicherungskopie auswählen können.


![Sicherungskopie erstellen](images/sicherungsk.png)


> #### primary::Hinweis
>
> Da die Sicherung der Datenbank immer auf dem Serverrechner abgelegt wird, habe Sie von einem Client nicht die Möglichkeit, durch Anklicken des Lupensymbols den Pfad auszusuchen. Sie können lediglich manuell den entsprechenden Pfad für den Serverrechner eintragen. Auch müssen Sie die Endung `.fbk` an den Dateinamen anfügen. Wenn keinen Speicherort und keinen Dateityp angeben wird die Sicherungskopie ohne Dateiendung im Verzeichnis System32 abgelegt.


Bei Dateiname geben Sie bitte eine Bezeichnung und einen Pfad Ihrer Wahl für diese Datei an, also beispielsweise `C:\Sicherung\Magellan6_011208.fbk`.


Wählen Sie im Feld Dateityp aus `Sicherungskopien (\*.fbk)`. Somit wird automatisch beim Speichervorgang diese Endung ergänzt. In unserem Beispiel würde somit an einem von Ihnen gewählten Speicherort eine Datei angelegt mit dem Namen `Magellan6_011208.fbk`.
Eine Sicherungskopie kann im laufenden Betrieb von Magellan durchgeführt werden.


> #### primary::Wichtig
>
> Von der Sicherungskopie sind alle Dokumente, WordVorlagen und Berichte ausgenommen.


#### Sicherungskopie wiederherstellen


Um eine bestehende Sicherungskopie wiederherstellen zu können, müssen Sie `Sicherungskopie wiederherstellen` wählen. Im Auswahlfeld Dateiname der Sicherungskopie kann man nun über das Lupensymbol den Explorer öffnen und hier die gewünschte Sicherungskopie (siehe `Sicherungskopie erstellen`) auswählen. Diese Sicherungskopie muss lokal auf dem Rechner liegen, an dem Sie den Rücksicherungsvorgang durchführen möchten. Der Vorgang gelingt nicht, wenn die Sicherungskopie in einem Netzwerkpfad abgespeichert wurde.


Im Feld `Dateiname der neuen Datenbank` kann man nun über das Lupensymbol den Explorer öffnen und einen Speicherplatz bestimmen sowie einen Namen für die wiederherzustellende Datenbank vergeben, also beispielsweise `Magellan`. Bitte achten Sie darauf, dass Sie bei Dateityp auswählen `Datenbankdateien (\*.fdb)`. Somit wird automatisch beim Speichervorgang diese Endung ergänzt. In unserem Beispiel würde an einem von Ihnen gewählten Speicherort eine Datei angelegt mit dem Namen Magellan6.fdb. Wenn Sie die wiederherzustellende Datei so benennen wie die aktive Datenbank, also in der Regel Magellan6.fdb, dann können Sie als Speicherort nicht den Datenbankordner wählen, da hier ja bereits eine Datei namens Magellan6.fdb existiert. Ein Ersetzen dieser bereits vorhandenen Datenbank durch die gleichnamige Wiederherstellungskopie wird an dieser Stelle verhindert, da sie ja im Rahmen der Sicherungsaktion in diesem Moment im Zugriff ist.


> #### primary::Hinweis
>
> Das Herstellen einer Sicherungskopie und anschließende Wiederherstellen dieser Sicherungskopie hat eine reparierende und zugleich komprimierende Funktion. Die wiederhergestellte Sicherungskopie ist stets kleiner als die Ausgangsdatenbank, da Lücken in der Datenbank beseitigt werden und so die Datenmenge `abgespeckt` wird. Wir empfehlen in Abständen die Realdatenbank mit einer wiederhergestellten Sicherung zu ersetzen. Bitte beachten Sie, dass beim Austausch der Datenbank immer der Firebird-Server gestoppt ist. Diesen Dienst können Sie stoppen und starten in der Systemsteuerung Ihres Servers im Aufruf Firebird Server Manager.


#### Einbinden der Sicherung in den Windows Taskplaner


Sie können die Aktion `Datenbanksicherungskopie erstellen` mit in den Taskplaner des Serverrechners einbinden. Damit könnten Sie sicherstellen, dass diese Aktion automatisch einmal täglich ausgeführt wird. Gehen Sie dafür bitte folgendermaßen vor:


Bitte erstellen Sie mit dem Texteditor eine neue Datei und kopieren den nachfolgenden Text hinein. Bitte beachten Sie, dass die Pfade bei Ihrer Installation abweichen können:




````C:\Program Files (x86)\Firebird\Firebird_2_5\bin\gbak.exe` -v -t -user SYSDBA -password masterkey -y `C:\Users\Public\Documents\Stueber Systems\Magellan 6\Datenbank\Backup\MAGELLAN6_%date:~0%.log` `C:\Users\Public\Documents\Stueber Systems\Magellan 6\Datenbank\MAGELLAN6.FDB` `C:\Users\Public\Documents\Stueber Systems\Magellan 6\Datenbank\Backup\MAGELLAN6_%date:~0%.FBK` pause```


Speichern Sie diesen Text und passen die drei Pfade den Gegebenheiten auf Ihrem Serverrechner an. Wir beschreiben nachstehend die Bedeutung der einzelnen Punkte:


Hinweis | Bedeutung
---------- | -------------
Pfad zur gbak.exe| Der erste Pfad führt zur gbak.exe, die die Datensicherung Ihrer Magellan6.fdb erstellt. Der von uns angebebene Pfad entspricht dem Standardinstallationspfad, könnte bei Ihnen aber abweichen.
-user und -password| Anschließend ist die Administratorenanmeldung an Ihrer Datenbank in der Datei enthalten, wenn Sie ein anderes Passwort verwenden, tragen Sie dieses anstelle von `masterkey`ein.
-y und Pfad|Dieser optionale Pfad legt Ihnen pro Sicherung eine Logdatei mit dem Tagesdatum mit den Meldungen an.
Pfad und Dateiname der *.fdb|Der nachfolgende Pfad verweist auf Ihre Datenbank. Liegt Ihre Datenbank an anderer Stelle, passen Sie diesen Pfad bitte an.
Ablagepfad der Sicherungskopie|Als letzte Information wird der Ablagepfad für die Sicherungskopie mit angegeben. Sie könnten sich einen gesonderten Unterordner `Backup` erstellen, müssten auf diesen dann im Pfad verweisen.
Pfad und Dateiname der *.fbk| Der Dateiname wird automatisch mit Magellan6_aktuelles Datum.fbk angegeben. Durch das Datum im Namen wird sichergestellt, dass die Sicherungskopie des Vortages nicht täglich überschrieben wird.
pause|Programmfenster im Vordergrund oder unsichtbar: Wenn Sie `pause` weglassen, dann läuft die Sicherung im Hintergrund ab, mit pause können Sie den Fortschritt im Vordergrund verfolgen. Wenn Sie eine Logdatei erstellen lassen, können Sie auf diesen Parameter verzichten.


Wenn alle Angaben angepasst sind, speichern Sie die Datei und benennen sie anschließend in `MagellanBackup.bat`um. Legen Sie diese Datei bitte auf Ihrem Server im Datenbankordner ab.


> #### primary::Datei testen
>
> Führen Sie die Datei zum Test bitte per ```Doppelklick``` oder ```Rechtsklick > Ausführen``` aus.


Klappte es? Dann richten Sie im Taskplaner bitte einen neuen Task ein, der täglich zu einer bestimmten Zeit diese Datei ausführt. Gehen Sie dazu auf dem Server unter: `Start > Programme > Zubehör > Systemprogramme > geplanteTasks`.


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


##### Voraussetzungen in der Benutzerverwaltung des MAGELLAN Administrators


Voraussetzung|Bemerkung
--|--
Teilnehmer von MAGELLAN|Unterkarte MyMAGELLAN, hier muss `Teilnehmer` gewählt werden
Rechtegruppe|Der Benutzer benötigt mindestens die Rechtegruppe Kollegium 1
Passwort für die Mym-Datei|Optional: als Kennwort kann das MAGELLAN-Kennwort oder ein gesondertes MyMAGELLAN-Kennwort verwendet werden.
Pfad zur Erzeugung der Mym-Datei|Auf der Unterkarte MyMAGELLAN in der Benutzerverwaltung muss für jeden Kollegen ein Pfad und ein Dateiname hinterlegt werden. An dieser Stelle wird später vom MyMAGELLAN-Center die mym-Datei erzeugt.


##### Voraussetzungen in MAGELLAN


Voraussetzung|Bemerkung
--|--
Lehrerzuweisung|mym-Dateien können für drei Lehrerrollen befüllt werden:<br/>- Tutor (erhält alle Fachzeilen des Schülers, kann weitere Daten editieren)<br/>- Klassenleiter (erhält alle Fachzeilen des Schülers, kann weitere Daten editieren)<br/>- Fachlehrer (erhält gezielt Fachzeilen des Schülers, kann weitere Daten nicht editieren)<br/> Je nach Rolle muss der Kollege auch zugewiesen werden: <br/>- ```Schüler > Zeugnis >Details > Tutor```<br/>- ```Klasse > Zeiträume >Zeitraum > Klassenleiter```<br/>- ```Schüler > Zeugnis > Fächer > Spalte Lehrer```
Schülerfächer|```Schüler > Zeugnis > Fächer ``` muss gefüllt sein


Eine ausführliche Anleitung finden Sie im Administrationsteil des das [MAGELLAN-Benutzerhandbuchs](http://doc.magellan6.stueber.de).



