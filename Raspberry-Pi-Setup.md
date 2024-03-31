# Installation Raspberry Pi

## Ce dont vous aurez besoin

* Une carte mini-SD (8-64gb)
* Un adapteur carte SD
* Un ordinateur d'accès (Windows, Mac ou Linux) (portable)
* Une connexion Wifi OU un fil usb-c
* Un raspberry pi (3-5)
* Un power supply du raspberry pi
  * Chargeur et fil usb-c
  * 2A minimum, 3A+ est mieux
  * Le rPi fonctionne à 5 volts
* (Facultatif) Fil HDMI<-->Mini-HDMI
* (Facultatif) Clavier-souris USB
* Logiciels (avoir les installeurs et les images déjà téléchargées sur votre ordinateur d'accès peut être très utile sur le terrain)
  * Raspberry Pi Imager [https://www.raspberrypi.com/software/](https://www.raspberrypi.com/software/)
  * Image rPi (1GB+)
  * MobaXterm version portable [https://mobaxterm.mobatek.net/download-home-edition.html](https://mobaxterm.mobatek.net/download-home-edition.html)(Choisir Version Portable)
    * ou Putty version portable EXE [https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)
  * VNC Viewer de RealVNC version StandAlone : [https://www.realvnc.com/fr/connect/download/viewer/](https://www.realvnc.com/fr/connect/download/viewer/)(Choisir version STANDALONE EXE)
  * Raspberry Pi Auto Hotspot [https://www.raspberryconnect.com/projects/65-raspberrypi-hotspot-accesspoints/203-automated-switching-accesspoint-wifi-network](https://www.raspberryconnect.com/projects/65-raspberrypi-hotspot-accesspoints/203-automated-switching-accesspoint-wifi-network)(Bien choisir la version selon votre RaspberryPi OS (différent si Bullseye, Buster ou Bookworm)) (verions présentes sur ce wiki)

## Liens intéressants

Documentation officielle de de la fondation Raspberry Pi:[https://www.raspberrypi.com/documentation/computers/getting-started.html](https://www.raspberrypi.com/documentation/computers/getting-started.html)

## Étapes

1. Préparer une carte SD avec une image de l'opérateur système
2. Ajuster des paramètres dans le dossier bootfs de la carte SD pour accéder le rPi sans écran, clavier ni souris

   1. Peut être ignoré si vous possédez une fil HDMI<-->Mini-HDMI, et un clavier/souris usb
3. Se connecter au Raspberry Pi par SSH puis par VNC(interface graphique)
4. Installer Raspberry Pi AutoHotspot

## 1. Préparer une carte SD avec une image de l'opérateur système

Veuillez suivre les instruction de ce site web. (Les PDF du site sont disponibles sur ce wiki)

[https://www.tomshardware.com/reviews/raspberry-pi-headless-setup-how-to,6028.html](https://www.tomshardware.com/reviews/raspberry-pi-headless-setup-how-to,6028.html)(Instructions en anglais, votre fureteur peut traduire ce site pour vous.)

Avec Raspberry Pi Imager, choisir l'image du OS qui convient au modèle que vous utiliserez.

Bien inscrire la connexion Wifi que vous allez utiliser. Soit un hotspot local de votre cellulaire, un modem LTE-wifi, ou le wifi de l'emplacement présent (bureau, etc). Notez que vous devrez inscrire le wifi terrain si vous ajouter celui du bureau en premier.

Choisir un nom d'utilisateur et mot de passe qui vous sera facile de retenir, et bien les noter. **Vous en aurez besoin pour vous connecter au rPi.

### Changements aux instructions du site fournis

Sélectionner la version du Raspberry Pi qui correspond à votre modèle.

## 2. Ajuster des paramètres dans le dossier bootfs de la carte SD

Ceci vous permettra de contrôler le Raspberry Pi sans y connecter d'écran, clavier ni souris.

Veuillez suivre les instruction de ce site web. (Les PDF du site sont disponibles sur ce wiki)

[https://www.tomshardware.com/reviews/raspberry-pi-headless-setup-how-to,6028.html](https://www.tomshardware.com/reviews/raspberry-pi-headless-setup-how-to,6028.html)(Instructions en anglais, votre fureteur peut traduire ce site pour vous.)

### Changements aux instructions du site fournis

Utiliser Putty version standalone  MobaXterm version portable au lieu de Putty si vous n\'avez pas accès au mode Administrateur de votre ordinateur d'accès

## 3. Se connecter au Raspberry Pi par SSH puis VNC

Pour contrôler le Raspberry Pi sans y connecter d'écran, de clanier ni de souris, on y accède par SSH, pour débuter et continuer la configuration. Ensuite, il sera accessible par VNC, qui est une interface graphique d'accès et de contrôle à distance.

Veuillez suivre les instruction de ce site web. (Les PDF du site sont disponibles sur ce wiki)

[https://www.tomshardware.com/reviews/raspberry-pi-headless-setup-how-to,6028.html](https://www.tomshardware.com/reviews/raspberry-pi-headless-setup-how-to,6028.html)(Instructions en anglais, votre fureteur peut traduire ce site pour vous.)

### Changements aux instructions du site fournis

Utiliser VNC Viewer de RealVNC version portable (standalone) au lieu de l'installation normale, si vous n\'avez pas accès au mode Administrateur de votre ordinateur d'accès.

## 4. Installer Auto Hotspot

Le Autohotspot est une installation qui permet au Raspberry Pi de devenir un Hotspot (fournisseur de connexion Wifi). Ce qui permet de s'y connecter par SSH-VNC s'il n'y a pas de connexion wifi présente sur le terrain. Fonctionne également si une connexion wifi (ou LTE) est accessible.

Suivre les instructions de ce site web. (Les PDF de ce site est disponibles sur ce wiki.)

[https://www.raspberryconnect.com/projects/65-raspberrypi-hotspot-accesspoints/203-automated-switching-accesspoint-wifi-network](https://www.raspberryconnect.com/projects/65-raspberrypi-hotspot-accesspoints/203-automated-switching-accesspoint-wifi-network) (Bien choisir la version selon votre RaspberryPi OS (différent si Bullseye, Buster ou Bookworm)) (verions présentes sur ce wiki)
