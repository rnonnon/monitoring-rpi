# Récupérer une image Raspbian
https://www.raspberrypi.org/downloads/raspbian/

# Activer ssh par défaut
Une fois la carte SD flashée avec Raspbian, créer un fichier nommé `ssh` sans extension à la racine de la carte SD

# Identifiants par défaut Rpi
**login:** pi

**pwd:** raspberry

# Lancer Ansible pour configurer les Rpi
`ansible-playbook init_rpi.yml -i inventory --ask-pass`

# Ajouter des Rpi managés
Modifier `inventory` en ajoutant les hosts souhaités et ajouter des fichiers de configuration pour chaque host dans `host_vars/NOM_DU_HOST.yml`

# Configurer les onglets chromium des Rpi
Changer les `chromium_tabs` dans `host_vars/NOM_DU_HOST.yml`

# Installer le plugin de rotation des onglets
Opération manuelle sur l'interface du raspberry
* Fermer le navigateur qui est actuellement en mode kiosk (ALT+F4)
* Ouvrir chromium (qui ne sera plus en mode kiosk)
* Installer le plugin `tab revolver` https://chrome.google.com/webstore/search/tab%20revolver?hl=fr
* Configurer le plugin
    * Durée de rotation
    * Empecher la rotation s'il y a eu des interactions sur l'onglet actif