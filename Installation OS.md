# MSI GE63VR 7RF Raider
Installation Xubuntu 18.04

## Download : 

- OS : [Xubuntu 18.04]( http://xubuntu.fr/)
- Utilitaire : [UNetbootin]( https://unetbootin.github.io/)

Créer une clé USB Live amorçable avec `UNetBootin`

## BIOS

Il est important de configurer la BIOS correctement afin d'éviter que le système gèle et soit compatible avec le noyaux Linux.
```
- Fast boot : Disaled
- Boot mode select : Legacy
- PCI Latency timer : 64 PCI Bus Clock
- Intel SpeedStep : Disaled
- Super Charger : Disabled
- ERP : Disabled
- Intel Virtualization : Enabled (virtualisation)
- VT-d : Enabled (virtualisation)
- CPU C-States : Disabled  (important !)
```

## Installation OS

ref: "https://forum.ubuntu-fr.org/viewtopic.php?id=1976971"

### 1. Démarrage sur la clé

Insérez la clé. 
Au moment où vous arrivez sur le menu, modifiez les options de démarrage ("TAB" ou "e" selon l'outil utilisé) 
afin d'y ajouter ceci, juste avant "quiet splash" :
```
nouveau.blacklist=1 acpi=off 
```

### 2. Installation:
Suivre les instructions d'installez `Xubuntu`

### 3. Premier démarrage:
Au redémarge pressez la touche `échap` ou `SHIFT` (si impossible d'accèder au GRUB remettre la clé usb bootable et pressez les touches précédament indiquer).
Comme pour le live USB, il faut modifier les options de démarrage.
Dans le GRUB pressez "e" et y ajouter :
```
nouveau.blacklist=1 acpi=off 
```
avant "quiet splash".
puis `CTRL+X`pour lancer le démarrage

### 4. Update:

* Redémarrez le PC ( modifiez une nouvelle fois les options de démarrage).
* Faire les mises à jour `Xubuntu`.
* Puis redémarrez le PC ( modifiez une nouvelle fois les options de démarrage).

### 5. Drivers nvidia

L'installation des pilotes nvidia :
```
sudo add-apt-repository ppa:graphics-drivers/ppa
sudo add-apt-repository ppa:kranich/cubuntu
sudo apt-get update
sudo apt-get install nvidia-367 nvidia-libopencl1-367 nvidia-opencl-icd-367 nvidia-prime nvidia-settings mesa-utils prime-indicator
```
