#Ubuntu-Server-VM erstellen

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
   
![Portweiterleitung](/Bilder/Portweiterleitung.png | width=100)

6. Eintrag wie im Bild hinzufügen 
   
![Portweiterleitung2](/Bilder/Portweiterleitung2.png | width=100)

© D.Zelger 