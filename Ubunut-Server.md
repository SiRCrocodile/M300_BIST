#Ubuntu-Server-VM

## Vagrantfile & VM erstellen
```shell
mkdir Ubuntu_Server
vagrant init ubuntu/trusty64
vagrant up --provider virtualbox

vagrant ssh
```

## Apache Webserver installieren
```shell
sudo apt-get install apache2
```
## Portweiterleitung einrichten
Beim Netzwerk ist unter NAT der Port 80 als Weiterleitung zu Port 8080 (Host) einzutragen
1. Virtualbox öffnen
2. rechte Maustaste auf VM "ändern"
3. Auf Reiter "Netzwerk"  wechseln
4. "Erweitert"
5. "Portweiterleitung"
   
![Portweiterleitung](/Bilder/Portweiterleitung.png)

1. Eintrag wie im Bild hinzufügen 
   
![Portweiterleitung2](/Bilder/Portweiterleitung2.png)

## Nützliche Befehle für Linux

**Administrator, Start und Stop Services und System**
```shell
sudo [-i] - Superuser werden, ein Password ist nicht erforderlich. –i = permanent
sudo service <servicename> start|stop - Starten und Stoppen eines Services z.B. apache2, mysql
sudo shutdown –r now - Restart des Betriebssystems
sudo shutdown –h now - Stoppen des Betriebssystems.
```

**Dateien bearbeiten und Filesystem**

```ls, rm, mv, cd ``` Anzeigen, löschen, verschieben von Dateien und Wechsel Verzeichnis
```nano oder [vi](http://debiananwenderhandbuch.de/vi.html)```Texteditoren
```df –h, free –m, w``` Diskbelegung, Speicherbelegung, Auslastung CPU


**Netzwerk**

```ifconfig``` Ausgabe der eigenen IP-Adresse
``` netstat -a oder netstat -tulpen ``` Ausgabe der verwendeten Network Ports
```net lookup <hostname>``` IP-Adresse für Hostname ausgeben.


**Prozesse**

```ps -ef oder top``` Anzeige der aktiven Prozesse
``` kill <pid>``` Prozess laut Prozess-Id (Nummer) beenden

**Hilfsprogramme**

```curl http://<server>``` Aufruf einer Webseite oder eines HTTP REST Services
```wget http://<server>/<datei>``` kopieren einer Datei von einem Webserver
```dos2unix <Datei>``` Datei vom DOS ins UNIX/Linux Format umwandeln. Wird immer dann benötigt wenn eine Datei von Windows nach     Linux kopiert wird und überflüssige CR enthält.




© D.Zelger 