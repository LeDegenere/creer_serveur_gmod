# 💻 Comande pour créer un serveur GMOD sur un VPS

# Installation des Prérequis 

`apt update`

`apt full-upgrade`

`sudo apt-get install lib32gcc-s1` (Cela est nécéssaire pour pouvoir lancer SteamCMD)

`apt update`

`sudo apt-get -y install screen` (Cela est nécéssaire pour pouvoir quitter Putty sans que le serveur GMOD s'éteingne)

# Installation de SteamCMD
`wget https://steamcdn-a.akamaihd.net/client/installer/steamcmd_linux.tar.gz`

# Extraire le fichier SteamCMD
`tar -xvzf steamcmd_linux.tar.gz`

# Installer UFW (Le Firewall qui va permettre d'ouvir les Ports pour GMOD)
`sudo apt-get install ufw`

# Ouvrir les ports pour GMOD
`sudo ufw allow 27015`

`sudo ufw allow 27015/udp`

`sudo ufw enable`
