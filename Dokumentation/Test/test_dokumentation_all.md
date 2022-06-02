## Git Repository anlegen

### Starten mit einem neuen Git-Repository 

Als erstes wird auf Github ein Repository erstellt. Danach bringen wir ein *vorhandenes, lokales Verzeichnis* unter **Git Versionskontrolle**, um diese beiden Repos anschliessend zu synchronisieren (verknüpfen). Ab dann können die lokalen Daten in das *remote Repository*  von [Github](https://github.com/) **"ge"pushed** - oder umgekehrt, die Daten von [Github](https://github.com/) in das lokale Repository **"ge"pulled** werden.

### Remote Git Repository erstellen

Vorbereitend für das **M431** erstellen wir auf [Github](https://github.com/) ein neues, **leeres** Repository, mit welchem wir weiter unten das lokale Repo verknüpfen

> Ein auf Github hinterlegter **SSH-PublicKey** des lokalen Benutzers/Rechner ist Voraussetzung <br>
> Genau so ist Voraussetzung, dass auf dem Rechner Git Bash installiert ist --> Hier der Download-Link [Git Bash download](https://git-scm.com/downloads)  <br>

Folgende Settings für das [Github](https://github.com/)-Repo sind vorgesehen

> `Repository name:  ` _M431_<br>
> `Description  ` _Aufträge im eigenen Berufsumfeld selbstständig durchführen_ <br>
> `Private:  ` _Repo auf "Private" setzen und später LP (weitere Contributors) einladen_<br>
> `Initialize this repository with:  ` _NICHTS ankreuzen - erfolgt zu einem späteren Zeitpunkt_ <br>

### Git Repository lokal anlegen/initialisieren

Zu beginn sollte man sich einen Pfad bzw. geeigneten Ort aussuchen wo man sein .git Verzeichnis haben möchte. <br>
Wenn man das hat geht man dort in das Verzeichnis rein -> Rechtsklick und auf **Git Bash Here** und dann ist man start klar.

Zuerst wird das Git Repo initialisiert, damit wir überhaupt irgenetwas mit Git anfangen können.

Hier habe ich noch verschiedene Vorgehensweisen wie man ein Repository erstellen kann:
![Repository lokal einrichten](images/Github-Repo_lokal_erstellen.PNG) <br>

Wir hatten noch kein existierendes Repository, somit haben wir eins von der Kommandozeile aus erstellt.
- Tipp: Lernt auf der Kommandozeile zu arbiten, vor allem bei Git, es wird euch vieles erleichtern.

Jetzt werde ich euch einige Snippets zeigen, wie wir unser Repository eingerichtet haben und Schritt für Schritt erklären was genau gemacht wird.

![Repository initialisieren](images/Git_init.PNG) <br>

![Status überprüfen](images/Git_status.PNG) <br>

![Erstes File erstellen --> README](images/touch_README.PNG) <br>

![Alle files für den Commit stagen](images/Git_add.PNG) <br>

![Git commit](images/Git_commit.PNG) <br>

![Ändern von Master auf Main](images/Git_branch.PNG) <br>

![Zum remote Repo hinzufügen](images/Git_add_remote_Repo.PNG) <br>
