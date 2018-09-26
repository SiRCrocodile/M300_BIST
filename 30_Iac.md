# Infrastructure as Code

Um einen Server, der Apache bereits vorinstalliert hat, kann man mit Hife von Vagrant diesen erstellen lassen.
Eine genau Reienfolge der Befehle folgt unten:

''shell
mkdir ubuntu_server_lb1
cd ubuntu_server_lb1
vagrant init
nano Vagrantfile
vagrant up
''

Dazu einen neuen Ordner am gwewünschten Ort erstellen. Dann in den Ordenr wechseln und mit "vagrant init" ein neues File erstellen. Im Vagrantfile folgenede Zeilen einfügen (Das File findet man auch im Ordner "Files"):

!Achtung: Das Vagrantfile verweist auf ein anderes File welches dafür sorgt das der Webserver auch installiert wird.

```shell

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.provision :shell, path: "bootstrap.sh"
  config.vm.network "forwarded_port", guest:80, host:8080, auto_correct: true
  
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "512"
    end
end
```
Das Bootstrap.sh-File beinhaltet folgende Zeilen (Das File findet man auch im Ordner "Files"):

```shell
#!/usr/bin/env bash

apt-get update
apt-get install -y apache2
if ! [ -L /var/www ]; then
  rm -rf /var/www
  ln -fs /vagrant /var/www
fi
```
Bevor die VM gestartet werden kann, sollte man im Verzeichnis noch einen Ordner mit dem Namen "html" erstellen. In disem Ordner könnt ihr nun sämtliche File für euren Webserver ablegen. Diese wird dann automatisch mit Apache synchronisiert.
Sind diese beiden Files erstellt und angepasst sind, kann man diese Speichern und mit dem Befehl "vagrant up" die VM starten. Ist dieser Vorgang abgeschlossen, sollte auf die Website über "localhost:8080" aufgerufen werden.

© D.Zelger 