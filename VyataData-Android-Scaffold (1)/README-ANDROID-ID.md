# Vyata Data — Android (Capacitor)

Project scaffold generated from the uploaded Vercel web source. It is **not an APK yet**.
The web app is bundled in `www/index.html`; Supabase remains a remote service, so device internet is required.

## Requirements
- Node.js LTS (includes npm)
- Android Studio with Android SDK installed
- JDK supported by the installed Android Gradle Plugin (Android Studio's bundled JDK is usually suitable)

## Build a debug APK on Windows
1. Extract this folder.
2. Open PowerShell in this folder.
3. Run:

   ```powershell
   npm install
   npm run android:add
   npm run android:sync
   npm run android:open
   ```

4. Android Studio opens the `android` project. Wait for Gradle sync to finish.
5. Select **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
6. The debug APK is usually created at `android\app\build\outputs\apk\debug\app-debug.apk`.

If the `android` folder already exists, skip `npm run android:add` and run `npm run android:sync`.

## Supabase and testing
- The source uses Supabase Auth/REST endpoints and browser `localStorage`. Test login, refresh/reopen, logout, reading/writing data, and role/RLS restrictions on a physical device.
- The publishable Supabase key in the web source is client-side by design; never put a Supabase `service_role` or secret key in this app.
- Ensure the Supabase RLS policies enforce permissions server-side. A hidden UI/admin role is not a security boundary.
- The source loads jsPDF, AutoTable, and SheetJS from public CDNs, so those features need internet access.
- The web app's data persistence and synchronization behavior should be tested on Android before production release.

## Important behavior
This build packages a copy of the current HTML source. Later changes deployed to Vercel do not automatically update the APK; rebuild and distribute a new APK to include those changes.
