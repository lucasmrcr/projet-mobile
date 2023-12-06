# Lucas Mercier

# CI
Les actions sont présentes dans le dossier `.github/actions`, elles sont utilisées dans les workflows présents dans le dossier `.github/workflows`.
Deux workflows sont présents :
- `develop.yaml` : Déclenché à chaque push sur la branche develop, il va lancer les tests unitaires et vérifier que le build se fait correctement.
- `release.yaml` : Déclenché à chaque création de tag sur marster, il va lancer les tests unitaires et faire un build. Ce build produit un fichier .apk et est envoyé sur le serveur distant dans le dossier `/home/lucas/projet-mobile/app-{version}.apk`.