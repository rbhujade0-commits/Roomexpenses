# Shared Expenses – Android app

A WebView wrapper around your Shared Expenses page (`app/src/main/assets/index.html`).
Firebase sync, login, edit/delete, charts and animations all work as in the browser.
CSV export saves to the phone's Downloads folder.

## Get the APK (easiest: no installs)
1. Create a free GitHub account and a new empty repository.
2. Upload everything in this folder (keep the `.github` folder) to the repository.
3. Open the **Actions** tab -> **Build APK** -> wait ~3 minutes.
4. Open the finished run, download **SharedExpenses-apk**, unzip it -> `app-debug.apk`.
5. Send it to your phone and install (allow "Install unknown apps" if asked).

## Or build on your PC
Install Android Studio, choose *Open* on this folder, then
*Build -> Build Bundle(s) / APK(s) -> Build APK(s)*.
The file appears in `app/build/outputs/apk/debug/app-debug.apk`.

## Update the app's page later
Replace `app/src/main/assets/index.html` with the new file and build again.

## Notes
- Fingerprint (WebAuthn) is not supported inside Android WebView, so the app falls back to username + password.
- The APK is signed with a debug key: fine for your own phones, not for Play Store.
