# MTv Pro 5.0 — Android TV, Google TV et Android

Version native de MTv dédiée à la lecture IPTV. Les rubriques WebView de l'édition Standard sont absentes. Le lecteur Media3/ExoPlayer, les playlists M3U, Xtream Codes, le guide TV, les favoris, l'historique et les contrôles parentaux sont conservés.

## Configuration de compilation vérifiée

- JDK 17
- Android Gradle Plugin 8.10.1
- Gradle 8.11.1
- Android SDK Platform 36
- Android Build Tools 36.0.0
- `applicationId: com.globaltv.pro`
- `namespace: com.globaltv.app`
- `minSdk 23`, `targetSdk 36`
- `versionName: 5.0.0`, `versionCode: 6`

## Compilation locale

Le dépôt ne contient pas de Gradle Wrapper. Installer Gradle 8.11.1 puis exécuter depuis ce dossier :

```bash
gradle lintDebug assembleDebug --no-daemon
```

Le workflow GitHub Actions `.github/workflows/build-apk.yml` installe JDK 17, Gradle 8.11.1 et les composants SDK Android 36. Il exécute Lint avant de compiler l'APK debug. Dans GitHub : **Actions → Build Android APK**. L'artefact produit est `mtv-pro-debug-apk`.

## Version Release

Aucune clé de signature de production n'est configurée dans le dépôt. La signature devra être ajoutée via les secrets GitHub avant toute publication. Ne jamais versionner le keystore ou ses mots de passe.

## Validation avant diffusion

Les builds CI ne remplacent pas les tests sur téléviseurs et téléphones réels : navigation D-pad, lecture et reprise des flux, buffering, formats d'écran, réseau instable et contrôles parentaux doivent être validés.
