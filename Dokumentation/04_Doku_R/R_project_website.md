# Git Repository anlegen


### Starten mit einem neuen Git-Repository

Als erstes wird auf Github ein Repository erstellt. Danach bringen wir ein *vorhandenes, lokales Verzeichnis* unter **Git Versionskontrolle**, um diese beiden Repos anschliessend zu synchronisieren (verknüpfen). Ab dann können die lokalen Daten in das *remote Repository*  von [Github](https://github.com/) **"ge"pushed** - oder umgekehrt, die Daten von [Github](https://github.com/) in das lokale Repository **"ge"pulled** werden.

---

### Remote Git Repository erstellen <br>

Vorbereitend für das **M431** erstellen wir auf [Github](https://github.com/) ein neues, **leeres** Repository, mit welchem wir weiter unten das lokale Repo verknüpfen

#### Voraussetzungen

  - [Github](https://github.com/) Account <br>
  - Ein auf Github hinterlegter **SSH-PublicKey** des lokalen Benutzers/Rechner ist Voraussetzung <br>
  - Windows: [GitBash](https://git-scm.com/downloads) auf dem lokalen Host installiert <br>
  - Editor: z.B: [Visual Studio Code](https://code.visualstudio.com/) , [Atom](https://atom.io/) oder [Sublime Text](https://www.sublimetext.com/) etc... <br>
  - Den Willen etwas neues zu **lernen** und so viel **Spass** haben wie möglich!!! :)

Folgende Settings für das [Github](https://github.com/)-Repo sind vorgesehen

> `Repository name:  ` _M431_<br>
> `Description:  ` _Aufträge im eigenen Berufsumfeld selbstständig durchführen_ <br>
> `Private:  ` _Repo auf "Private" setzen und später LP (weitere Contributors) einladen_<br>
> `Initialize this repository with:  ` _NICHTS ankreuzen - erfolgt zu einem späteren Zeitpunkt_ <br>

---

### Git Repository lokal anlegen/initialisieren

Zu beginn sollte man sich einen Pfad bzw. geeigneten Ort aussuchen wo man sein .git Verzeichnis haben möchte. <br>
Wenn man das hat geht man dort in das Verzeichnis rein -> Rechtsklick und auf **Git Bash Here** und dann ist man start klar.

Zuerst wird das Git Repo initialisiert, damit wir überhaupt irgenetwas mit Git anfangen können.

Hier habe ich noch verschiedene Vorgehensweisen wie man ein Repository erstellen kann:
![Repository lokal einrichten](images/Github-Repo_lokal_erstellen.PNG) <br>

Wir hatten noch kein existierendes Repository, somit haben wir eins von der Kommandozeile aus erstellt.
- **Tipp**: Lernt auf der Kommandozeile zu arbiten, vor allem bei Git, es wird euch vieles erleichtern.

Jetzt werde ich euch einige Befehle zeigen, wie wir unser Repository eingerichtet und Schritt für Schritt erklären was genau gemacht wurde.

#### Commands die wir verwenden müssen (lokal auf der Gitbash)

> `$ cd <Projektverzeichnis> ` _irgend ein Verzeichnis, welches **nicht** unter Git Kontrolle ist_<br>
> `$ mkdir M431_Repository  ` _künftiges Repository-Verzeichnis erstellen_ <br>
> `$ cd M431_Repository  ` _Ins Repository-Verzeichnis wechseln_ <br>
> `$ git init  ` _Lokales Git-Repo initialisieren (erstellt .git-Verzeichnis)_ <br>
> `$ ls -lisa ` _nach dem *init* Befehl existiert neu das .git Verzeichnis, welches u.a. das locale Repository enthält_

#### Erster Commit im lokalen Repository (lokal auf der Gitbash)
Mit den folgenden Kommandos wird ein erstes File (in unserem Fall das README.md) im getrackten Verzeichnis erstellt, ge"stage"d und commited. Mit dem "Commit" wird der aktuelle Stand in mein lokales Repository eingepflegt. 

> `$ echo "# M431 Dokumentation " >> README.md  ` _File "README.md" mit Titel erstellen_ <br>
> `$ git add .   ` _Added alle Files im aktuellen Verzeichnis zur "Staging area"_ <br>
> `$ git add README.md` _Added nur die Files, die man angibt, in diesem Fall das README.md_ <br>
> `$ git commit -m "First Commit"` _Files werden ab jetzt lokal getracked_ <br>
> `$ git log` _Log Eintrag des eben ausgeführten Commits zeigen_ <br>

#### Synchronisation des lokalen Repos mit dem Github-Repository (Origin)
...jetzt muss das lokale Repository mit dem Remote-Repository gesynched werden, damit das kollaborative Arbeiten daran ermöglicht werden kann. Im nächsten Schritt wird das lokale Repository mit dem Github-Repository einmalig "verlinkt". Danach kann das Repository jeweils **ge"pushed"**, **ge"pulled"**, **ge"klont"**, **ge"forked"** oder **ge"branched"** werden. <br>

Dies geschieht mit folgenden Kommandos:

> `$ git remote add origin https://github.com/<Benutzername>/M431.git   ` _Verlinken der Repos_ <br>
> `$ git branch -M main   `_Ändert den branch von Master zu main_ <br>
> `$ git push -u origin master   ` _Github-Passwort eingeben und hochladen_ <br>

---

Alle Kommandos, wie sie in der richtigen Reihenfolge eingegeben werden:

`$ cd <Projektordner>` <br>
`$ git init` <br>
![Repository initialisieren](images/Git_init.PNG) <br>
`$ git status` <br>
![Status überprüfen](images/Git_status.PNG) <br>
`$ git status` _Wenn nach dem commit etwas verändert, hinzugefügt oder gelöscht wurde_ <br>
![Status überprüfen](images/status_before_commit.PNG) <br>
`$ git status` _Sobald alle Files wieder in der Staging Area sind_ <br>
![Status überprüfen](images/status_after_add.PNG) <br>
`$ touch README.md` <br>
![Erstes File erstellen --> README](images/touch_README.PNG) <br>
`$ git add README.md` <br>
![Alle files für den Commit stagen](images/Git_add.PNG) <br>
`$ git commit -m "first commit"` <br>
![Git commit](images/Git_commit.PNG) <br>
`$ git branch -M main` <br>
![Ändern von Master auf Main](images/Git_branch.PNG) <br>
`$ git remote add origin https://github.com/<Benutzername>/M431.git` <br>
![Zum remote Repo hinzufügen](images/Git_add_remote_Repo.PNG) <br>
`$ git push -u origin main` <br>
![pushed alles in (origin) Repo](images/Git_push.PNG) <br>

---

#### Summary

- Zuerst wurde das Git-Repo "M431" lokal und remote erstellt und verlinkt (Daten werden ab diesem Zeitpunkt ge"**tracked**" und können ge"**pushed**" oder ge"**pulled**" werden). 
- Im lokalen Git-Repository wurde das File "README.md" erstellt und commited. Daten im Verzeichnis werden nun also **lokal** verwaltet und getrackt.
- Abschliessend wurde mit dem "git push"-Kommando der aktuelle lokale Repo-Inhalt zum **"Origin"** (Github-Repo, Remote) übertragen.  

**Ab diesem Zeitpunkt sind wir bereit, um das Repository aktiv zu bewirtschaften - **IaC** (Infrastructure as Code) ready.**

---
