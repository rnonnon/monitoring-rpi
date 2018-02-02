# R�cup�rer une image Raspbian
https://www.raspberrypi.org/downloads/raspbian/

# Activer ssh par d�faut
Une fois la carte SD flash�e avec Raspbian, cr�er un fichier nomm� `ssh` sans extension � la racine de la carte SD

# Identifiants par d�faut Rpi
**login:** pi

**pwd:** raspberry

# Lancer Ansible pour configurer les Rpi
`ansible-playbook init_rpi.yml -i inventory --ask-pass`

# Ajouter des Rpi manag�s
Modifier `inventory` en ajoutant les hosts souhait�s et ajouter des fichiers de configuration pour chaque host dans `host_vars/NOM_DU_HOST.yml`

# Configurer les onglets chromium des Rpi
Changer les `chromium_tabs` dans `host_vars/NOM_DU_HOST.yml`

# Installer le plugin de rotation des onglets
Op�ration manuelle sur l'interface du raspberry
* Fermer le navigateur qui est actuellement en mode kiosk (ALT+F4)
* Ouvrir chromium (qui ne sera plus en mode kiosk)
* Installer le plugin `tab revolver` https://chrome.google.com/webstore/search/tab%20revolver?hl=fr
* Configurer le plugin
    * Dur�e de rotation
    * Empecher la rotation s'il y a eu des interactions sur l'onglet actif