# MSI GE63VR 7RF Raider

## Curl
```
sudo apt update
sudo apt install curl
curl --version
```

## Git
```
sudo apt update
sudo apt install git
git --version
```

## Zsh
### 1. Installation
```
sudo apt install zsh
sudo apt install git-core
sudo wget https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O - | zsh
```
OU

[oh-my-zsh](https://ohmyz.sh/) - site officiel

### 2. Paramétrage

Pour définir Zsh par défaut pour le terminal:
```
sudo chsh -s `which zsh`
sudo reboot
```
