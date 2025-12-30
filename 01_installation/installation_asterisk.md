# Installation d’Asterisk sur Debian
# Installation d’Asterisk sur Debian

Ce document décrit **l’installation complète d’Asterisk** sur Debian, étape par étape, avec toutes les commandes utilisées.  

---
```bash

## Étape 1 : Mise à jour du système
apt update && apt upgrade -y
----------------------------------------------------------------------------------------
## Étape 2 :Installation des prérequis
apt-get install unzip git gnupg2 curl libedit-dev libnewt-dev libssl-dev \
libncurses5-dev subversion libsqlite3-dev build-essential libjansson-dev \
libxml2-dev uuid-dev subversion -y
-------------------------------------------------------------------------------------
Étape 3 : Télécharger Asterisk-Déplacer ensuite dans le répertoire /usr/local pour la suite :
wget http://downloads.asterisk.org/pub/telephony/asterisk/asterisk-20-current.tar.gz
---------------------------------------------------------------------------------------------------
Étape 4 : Décompresser l’archive
tar -xvzf asterisk-20-current.tar.gz
----------------------------------------------------------------------------------------------------
Étape 5 : Préparation et dépendances supplémentaires
cd asterisk-20.2.1
contrib/scripts/get_mp3_source.sh
contrib/scripts/install_prereq install
------------------------------------------------------------------------------------------------------
Étape 6 : Configuration
./configure
------------------------------------------------------------------------------------------------------

Étape 7 : Sélection des modules
make menuselect
--------------------------------------------------------------------------------------------------------
Étape 8 : Installation
make install
--------------------------------------------------------------------------------------------------------
Étape 9 : Installer les fichiers exemples
make samples
---------------------------------------------------------------------------------------------------------
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
                       fin de l' installation du server asterisk
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++



