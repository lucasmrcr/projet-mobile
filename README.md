# Lucas Mercier

# CI
Les actions sont présentes dans le dossier `.github/actions`, elles sont utilisées dans les workflows présents dans le dossier `.github/workflows`.
Deux workflows sont présents :
- `develop.yaml` : Déclenché à chaque push sur la branche develop, il va lancer les tests unitaires et vérifier que le build se fait correctement.
- `release.yaml` : Déclenché à chaque création de tag sur marster, il va lancer les tests unitaires et faire un build. Ce build produit un fichier .apk et est envoyé sur le serveur distant dans le dossier `/home/lucas/projet-mobile/app-{version}.apk`.

# Description workflows
## develop.yaml
- Déclenché à chaque push sur la branche develop
- Lance les tests unitaires

## release.yaml
- Déclenché à chaque création de tag sous format `[0-9]+.[0-9]+.[0-9]+` sur master
- Clone le projet
- Télecharge les dépendances du projet
- Lance les tests unitaires
- Lance le build de l'application en APK
- Envoie l'APK sur le serveur distant dans le dossier `/home/lucas/mobile/app-{version}.apk`

# Installation
## Prérequis
- Téléphone android

## Installation
- Télécharger le fichier .apk sur le téléphone
- Lancer le fichier .apk
- Accepter les permissions
- Lancer l'application