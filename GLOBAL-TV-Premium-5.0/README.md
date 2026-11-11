# MTv Pro — Android TV, Google TV et Android

Version native de MTv dédiée à la lecture IPTV. Les sept rubriques WebView (AOXTv, WiTv, FrSTv, FsLive, EpiXtv, DudeTV et Braflix) ont été retirées. Le lecteur Media3/ExoPlayer, les playlists M3U intégrées (France et Afrique), Xtream Codes, le guide TV, les favoris, l'historique et les contrôles parentaux sont conservés.

## Compilation
JDK 17, Android SDK Platform 35 et Gradle 8.9. Le workflow GitHub Actions compile l'APK à chaque push sur `main` et publie l'artefact `mtv-pro-debug-apk`.

Projet dérivé de MTv (`MauriceStar/Mtvi`). Application indépendante avec l'identifiant Android `com.globaltv.pro`.