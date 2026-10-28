# Gym Log — Build an Android APK

This project packages the Gym Log web app as an Android app using Capacitor.

## Build an installable APK using GitHub Actions

This repository includes `.github/workflows/build-apk.yml`, which builds a debug APK in GitHub's hosted build environment.

1. Sign in to GitHub and create a new repository, for example `gym-log`.
2. Extract this ZIP on your computer.
3. Upload **all files and folders** from the extracted project to the repository root. Make sure `.github/workflows/build-apk.yml` is included.
4. Open the repository's **Actions** tab. If prompted, enable GitHub Actions.
5. Select **Build APK** and click **Run workflow**. If the workflow has not appeared yet, commit/push the files first and refresh the Actions tab.
6. Wait for the run to finish successfully.
7. Open the completed run and download the **gym-log-apk** artifact. Extract the downloaded artifact ZIP to find `app-debug.apk`.
8. Transfer the APK to an Android phone and open it to install. Android may ask you to allow installation from that source.

## What this build is

The workflow produces a **debug APK** for direct testing/sideloading. It is not a Play Store release. Keep in mind that users must trust the APK source, and Android may show an unknown-source installation warning.

## Notes

- App ID: `com.gymlog.tracker`
- App name: `Gym Log`
- The app stores workout and weight data in the device's local browser storage. Data is not automatically synced between devices.
- If the GitHub Actions build fails, open the failed run's log and check the first failing step.
