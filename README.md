# mobile

Application Android native écrite en **Kotlin** avec **Jetpack Compose** (Material 3).

## Prérequis

- [Android Studio](https://developer.android.com/studio) (version récente)
- JDK 17 (fourni avec Android Studio)
- Android SDK 35

## Démarrer

1. Ouvrir le dossier du projet dans Android Studio.
2. Laisser Gradle synchroniser le projet.
3. Lancer l'application sur un émulateur ou un téléphone (bouton ▶ *Run*).

En ligne de commande :

```bash
./gradlew assembleDebug        # construit app/build/outputs/apk/debug/app-debug.apk
./gradlew installDebug         # installe sur l'appareil connecté
./gradlew testDebugUnitTest    # lance les tests unitaires
```

## Structure

```
app/
  src/main/java/com/labaffe/mobile/
    MainActivity.kt        # point d'entrée + écran d'accueil
    ui/theme/Theme.kt      # thème Material 3 (clair / sombre / couleurs dynamiques)
  src/main/res/            # ressources (textes, thèmes…)
  src/test/                # tests unitaires
gradle/libs.versions.toml  # versions des dépendances
```

## Intégration continue

Le workflow `.github/workflows/android.yml` lance les tests et construit l'APK debug à chaque push ;
l'APK est téléchargeable dans les artefacts de l'exécution GitHub Actions.

## Configuration

- Package : `com.labaffe.mobile`
- minSdk 26 (Android 8.0) · targetSdk 35
