# M300_BIST

## Bash
Bash (für Bourne-again shell)) ist eine freie Unix-Shell und Teil des GNU-Projekts. Sie ist heute auf vielen unixoiden Systemen die Standard-Shell.
Bash wird Verwendet zur Ausführung von Shellscripts und zum Einloggen (via ssh) auf die Virtuellen Maschinen.

## GIT
Git ist eine freie Software zur verteilten Versionsverwaltung von Dateien, die durch Linus Torvalds initiiert wurde.
Git wird Verwendet als Client zu Versionsverwaltungssystemen.

### Command line instructions
``` shell
git global setup
git config --global user.name "<username>"
git config --global user.email "<mail>"
```

### Create a new repository
```shell
cd M300
git clone git@gitlab.com:git@github.com:SiRCrocodile/M300_BIST.git
touch README.md
git add README.md
git commit -m "add README"
git push -u origin master
```

### Existing folder
```shell
cd existing_folder
git init
git remote add origin git@github.com:SiRCrocodile/M300_BIST.git
git add .
git commit -m "Initial commit"
git push -u origin master
```

### Existing Git repository
```shell
cd existing_repo
git remote rename origin old-origin
git remote add origin git@github.com:SiRCrocodile/M300_BIST.git
git push -u origin --all
git push -u origin --tags
```
### Git- Befehlsreihenfolge
```shell
1. git status
2. git add -A
3. (git status)
4. git commit -m "Kommentar"
5. (git status)
6. git push
```

## VirtualBox 
VirtualBox ist eine Virtualisierungssoftware und erlaubt es, lokal auf dem PC sogenannte Virtuelle Maschinen zu Erstellen und zu Verwalten.
VirtualBox wird verwendet weil das Zusammenspiel mit vagrant am Besten funktioniert und die Software frei Verfügbar ist (Open Sourcen).

## Vagrant 
Vagrant ist eine Open-Source Ruby-Anwendung zum Erstellen und Verwalten von virtuellen Maschinen, mittels sogenannten Vagrantfiles.

### How to Vagrant

#### Neue VM erstellen 
Bash starten, neues Verzeichnis erstellen, Vagrantfile erzeugen und Virtuelle Maschine (VM) erstellen und starten:
```shell
mkdir ubuntu
cd ubuntu
vagrant init ubuntu/xenial64
vagrant up --provider virtualbox
```

Oder - wenn ein interner Server vorhanden ist:

```shell
vagrant box add http://10.1.66.11/vagrant/ubuntu/xenial64.box --name ubuntu/xenial64
vagrant init ubuntu/xenial64
vagrant up --provider virtualbox
```

#### Bestehende VM starten
```shell
cd existing_folder
vagrant up --provider virtualbox
vagrant ssh
```
#### Auf VM zugreifen
```shell
vagrant ssh
```
#### Zugriff auf VM beenden
```shell
exit
```
#### VM herunterfahren 
```shell
vagrant halt
```

#### VM löschen
```shell
vagrant destroy -f
```


## Markdown
Markdown ist eine vereinfachte Auszeichnungssprache, die von John Gruber und Aaron Swartz entworfen und im Dezember 2004 mit Version 1.0.1 spezifiziert wurde. Ein Ziel von Markdown ist, dass schon die Ausgangsform ohne weitere Konvertierung leicht lesbar ist. Als Auszeichnungselemente wurden daher vor allem Auszeichnungsarten verwendet, die in Plain text und E-Mails üblich sind. Auch andere Auszeichnungssprachen mit ähnlichen Zielen zur Lesbarkeit – wie reStructuredText oder Textile – hatten Einfluss auf die Syntax

[`Markdown Cheatsheet`](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#lists)


©D.Zelger
