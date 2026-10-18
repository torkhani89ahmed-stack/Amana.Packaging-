# AMANA PACKAGING — application Android (APK)

Application de gestion de stock, ventes et factures, empaquetée en APK avec Capacitor et compilée automatiquement par GitHub Actions.

## Contenu

- `www/index.html` : l'application
- `capacitor.config.json` et `package.json` : configuration Capacitor
- `.github/workflows/build-apk.yml` : compilation automatique de l'APK

## Obtenir l'APK

1. Créez un dépôt sur GitHub (privé de préférence, car l'application contient le logo de la société).
2. Envoyez-y tous les fichiers de ce dossier, en gardant la même arborescence (y compris le dossier `.github`).
3. Ouvrez l'onglet **Actions** du dépôt. La compilation démarre toute seule à chaque envoi ; vous pouvez aussi la lancer avec **Run workflow**.
4. Quand la tâche est verte (environ 5 à 10 minutes), ouvrez-la et téléchargez **amana-packaging-apk** en bas de page (fichier zip contenant `app-debug.apk`).
5. Copiez l'APK sur le téléphone et installez-le (autoriser les sources inconnues si Android le demande).

## Mettre à jour l'application

Remplacez `www/index.html` par la nouvelle version, envoyez-le sur GitHub : un nouvel APK est construit.

## Remarques

- L'APK généré est de type « debug » : il convient pour une installation directe. Pour le Play Store, il faut un APK/AAB signé (clé de signature à ajouter en secrets GitHub).
- Les données sont enregistrées sur le téléphone. Faites régulièrement une sauvegarde depuis Paramètres > Sauvegarde. Désinstaller l'application efface les données.
- L'icône de l'application est générée automatiquement à partir des images du dossier `assets/` (`icon-only.png`, `icon-foreground.png`, `icon-background.png`). Pour la changer, remplacez ces fichiers (1024×1024).
