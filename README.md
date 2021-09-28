# OpenSUSE
## Configuration d'OpenSUSE sur mon PC Lenovo Ideadpad 330-15ARR

### 1. À faire dès la distribution installée
#### a) Ajouter les dépôts communautaires packman & mettre packman comme dépôt principal
##### Première ligne de commande : 
* sudo zypper ar -cfp 90 https://ftp.gwdg.de/pub/linux/misc/packman/suse/openSUSE_Tumbleweed/ packman
##### Seconde ligne de commande : 
* sudo zypper dup --from packman --allow-vendor-change

#### b) Installation driver ethernet (packman doit être installé avant)
* sudo zypper in r8168-kmp-default
* sudo zypper in r8168-blacklist-r8169

## Lignes de commande à connaître
### 1. Zypper
#### a) Mises à jour
* sudo zypper refresh (rafraichir les dépots)
* sudo zypper up (faire les mises à jour des logiciels)
* sudo zypper dup (faire la mise à jour de la distribution)

#### b) Supprimer un logiciel et des dépendances
* sudo zypper rm --clean-deps 'nom du logiciel', sudo zypper rm -u 'nom du logiciel' (supprimer un package avec ses dépendances)
* zypper packages --unneeded (trouver des packages qui ne sont probablement plus nécessaires)

### 2. Flatpak
#### a) Lister les paquets
* flatpak list
#### b) Installer un logiciel
* flatpak install 'nom du logiciel'
#### c) Désinstaller un logiciel
* flatpak uninstall 'nom du logiciel'

##KDE
### 1. Lignes de commmandes
* kdesu systemsettings5 (ouvrir le configuration système en tant qu'administrateur)
