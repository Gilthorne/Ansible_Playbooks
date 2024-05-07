# TL1Ansible

Ceci est la documentation d'Ansible faite par Edouard Garnier pour le POD1, mes missions étant la gestion des switchs et routeurs cisco

# Installation d'Ansible sur la machine Mère
Voici comment installer ansible sur la machine mère:

Sudo apt install openssh-server 

sudo apt install python3

sudo pip3 install ansible (Pour avoir Ansible à la dernière version)

sudo ansible-galaxy collection install cisco.ios (Collection que j'utilise pour récupérer différents modules que j'utiliserais dans mes scripts).


# Connexion en ssh de la machine mère vers les switchs et le routeur pour échanger les clés et qu'Ansible puisse s'y connecter en ssh

Pour les switchs:

ssh -oKexAlgorithms=+diffie-hellman-group1-sha1 -oHostKeyAlgorithms=+ssh-rsa -c aes128-cbc user@ip

Pour le routeur:

ssh -oKexAlgorithms=+diffie-hellman-group1-sha1 -oHostKeyAlgorithms=+ssh-rsa -c aes128-ctr user@ip
