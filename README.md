# Pulse & Pressure for Android

A private, offline blood-pressure and heart-rate tracker designed for the Samsung Galaxy Z Fold family.

## Privacy design

- The Android manifest does **not** request internet access.
- Readings are stored only in the installed app's private local storage.
- No analytics, account, cloud database, ads, or external services are included.
- Android cloud backup is disabled for this app.
- Uploading this source project to GitHub does not upload your readings.
- Uninstalling the app or clearing its app data permanently removes its readings.

## Features

- Daily, 7-day, 14-day, and 28-day BP and heart-rate averages
- Multiple readings per day, with daily averaging
- Date, time, measurement context, and optional notes
- Reading history and deletion controls
- Folded and unfolded responsive layouts
- Fully offline operation

## Build an APK automatically with GitHub

1. Create a new GitHub repository.
2. Upload **the contents of this folder** to the repository's top level.
3. Open the repository's **Actions** tab.
4. Select **Build Android APK**, then choose **Run workflow**. It also runs automatically after a push to `main`.
5. When the workflow finishes, open the completed run.
6. Under **Artifacts**, download `PulsePressure-APK`.
7. Unzip it to get `app-debug.apk`.

## Install on the Galaxy Z Fold

1. Transfer `app-debug.apk` to the phone.
2. Open it from **My Files**.
3. If Android asks, allow **Install unknown apps** for My Files only.
4. Tap **Install**, then turn that permission back off afterward.

The debug APK is suitable for your personal installation. For Play Store distribution or long-term signed releases, create a private signing key in Android Studio and protect it carefully—never commit the key or its password to GitHub.

## Build with Android Studio

Open this folder in a current Android Studio version, let Gradle sync, then select **Build → Build APK(s)**. The project uses Java 17, Android Gradle Plugin 8.7.3, compile SDK 35, and supports Android 8.0 or newer.

## Important health note

This app organizes measurements; it does not diagnose or replace medical care. Discuss concerning or unusual readings with a qualified healthcare professional.
