# System Xubuntu

## Screenshot
`logiciel` > `Kazam`

## Casque avec un son faible / Headset with a weak sound
```
sudo alsamixer
```
 - J'ai sélectionné avec les flèches du clavier (right / left) `Speaker` 
 - Puis augmenter le son du casque avec les flèches du clavier (up / down).


![alt text](https://github.com/masselit/MSI-GE63VR-7RF-Raider/blob/master/doc/Capture%20d'%C3%A9cran%202018-07-18%2023:34:34.png)


open file '.zshrc'


end file enter `alias sound="alsamixer"`

## HDMI not sound
ref: [site](http://forum.kubuntu-fr.org/viewtopic.php?id=2027621)
download : [here](https://bugs.freedesktop.org/attachment.cgi?id=136418&action=edit)

`make
sudo make install
echo nvhda | sudo tee -a /etc/initramfs-tools/modules
echo "options nvhda load_state=1" | sudo tee /etc/modprobe.d/nvhda.conf
sudo update-initramfs -u`
