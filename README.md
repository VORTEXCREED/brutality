# FBI WALLET — Android app (Capacitor)
Preview build with demo balances. Same app as the desktop version, with a phone layout (bottom tabs, card-style asset list).

## Easiest: build the APK online (no installs)
1. Create a free GitHub account and a new repository.
2. Upload everything in this folder (keep the `.github` folder).
3. Open the repo's **Actions** tab → **Build APK** → wait ~5 min.
4. Download **FBI-WALLET-apk** from the run, unzip it, and send `app-debug.apk` to your phone.
5. On the phone, open the file and allow "Install unknown apps" when asked.

## Or build on your PC
Install Node 20, JDK 17 and Android Studio (for the SDK), then:
```
npm install
npx cap add android
npx cap sync android
cd android && gradlew assembleDebug
```
APK: `android/app/build/outputs/apk/debug/app-debug.apk`

## Notes
- This is a debug-signed APK, fine for sideloading and screen recording. A Play Store release needs your own signing key.
- Data saves inside the app. "Export JSON" may not download on some Android versions; the rest works normally.
- Edit www/index.html to change the app, then re-run the build.
