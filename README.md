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

# Installer iptables (Le Firewall qui va permettre d'ouvir les Ports pour GMOD)
`sudo apt-get install iptables-persistent`

# Ouvrir les ports pour GMOD
`sudo iptables -A INPUT -p udp --dport 27015 -j ACCEPT`

`sudo iptables -A INPUT -p udp --dport 27015:27030 -j ACCEPT`

`sudo iptables -A INPUT -p tcp --dport 27015:27030 -j ACCEPT`

`sudo iptables -A INPUT -p tcp --dport 27005 -j ACCEPT`
