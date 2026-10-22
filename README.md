# MangaFlow Android

MangaFlow is a native Android manga reader project with a live MangaDex catalog, search, cover art, English chapter lists, a vertical chapter reader, a saved library, and chapter image downloads to app-private storage. It is an independent reader and uses MangaDex's public API; available titles and translations depend on that source. Use content you are authorized to access.

## Build an APK with Android Studio

1. Install Android Studio on a computer and open this project folder.
2. Let Gradle sync and install the Android SDK platform requested by the project (API 35).
3. Select **Build → Build Bundle(s) / APK(s) → Build APK(s)**.
4. The debug APK is generated at `app/build/outputs/apk/debug/app-debug.apk`.

## Build an APK in GitHub Actions

A workflow is included at `.github/workflows/build-apk.yml`.

1. Create a GitHub repository and upload the contents of this folder to its `main` branch.
2. Open the repository's **Actions** tab and choose **Build MangaFlow APK**.
3. Tap **Run workflow** and wait for the job to finish.
4. Open the completed run and download the `MangaFlow-debug-apk` artifact. Unzip it to get `app-debug.apk`.
5. Transfer the APK to your Android phone and install it. Android may ask you to allow installs from the browser or file manager you used.

## Important notes

- This project has not been compiled or tested in this environment because Android SDK/Gradle build tools are unavailable here.
- The build workflow produces a debug APK, not a Play Store release. Do not install APKs from repositories you do not trust.
- Network access is required for browsing and loading new chapters. Downloaded chapter images are saved in the app's private storage.
- MangaDex API access, title availability, translation languages, and content ratings are controlled by MangaDex and may change.
