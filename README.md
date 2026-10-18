# COURTSIDE — Card Club (Android project)

This Android wrapper packages the existing offline game as a native-installable Android app. The game HTML and its embedded card artwork are stored in `app/src/main/assets/index.html`; no internet permission or runtime network access is required. Game progress is stored by the WebView using local storage.

## Build the APK using only an Android phone

This project includes a GitHub Actions workflow that builds a debug APK in the cloud. You need a GitHub account; the build itself runs online, so you do not need a computer or Android Studio.

1. Download and unzip `COURTSIDE_Android_Project.zip`.
2. In your phone browser, open GitHub and create a new **public or private repository** named `courtside-card-club`.
3. Upload the *contents* of the unzipped folder to the repository root, including the hidden `.github/workflows/build-apk.yml` file. If your phone's upload interface hides `.github`, use GitHub's web editor to create `.github/workflows/build-apk.yml` and paste the workflow from this project.
4. Open the repository's **Actions** tab, select **Build COURTSIDE APK**, then tap **Run workflow**. If prompted, enable Actions for the repository.
5. When it finishes successfully, open the completed run and download the artifact named `COURTSIDE-Card-Club-APK`. Extract the ZIP to get `app-debug.apk`.
6. Tap `app-debug.apk` on your phone to install. Android may ask you to allow your browser or file manager to install apps from that source. Only install APKs you built or trust.

## Notes
- This is a debug APK for personal testing, not a signed Play Store release.
- The first build needs internet because cloud build downloads Android build tools. Once installed, the game itself works offline.
- The game currently uses the existing prototype's simulated matches and card collection. This wrapper does not magically turn those into a full 3D basketball simulation.
- The icon vector is included as a drawable; if you want a custom launcher icon on all Android launchers, additional adaptive icon resources can be added later.
