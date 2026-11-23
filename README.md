# USM Yard Stock — Android WebView app

This Android app opens `https://furnacestock.ai.studio/` inside an Android WebView. It is online-only and keeps the website's server-side data and login behavior on the website. It does not create a separate stock database.

## Build the APK using only an Android phone

1. Download and extract this ZIP on your phone (Files app or a ZIP extractor).
2. Sign in or create a GitHub account at https://github.com/.
3. In GitHub, create a **New repository** named `usm-yard-stock`. For the simplest setup, make it **Private**.
4. Open the new repository, choose **Add file → Upload files**, and upload the *contents* of this extracted folder. Make sure `.github/workflows/build-apk.yml` is included. If GitHub's mobile page hides dot-folders, use the GitHub website in Chrome's **Desktop site** mode.
5. Commit the uploaded files to the `main` branch.
6. Open the repository's **Actions** tab. Select **Build USM Yard Stock APK** and tap **Run workflow** if it has not started automatically.
7. Wait for the workflow to finish with a green check mark. Open the completed run and scroll to **Artifacts**.
8. Download `USM-Yard-Stock-APK`. Extract the downloaded artifact ZIP to get `app-debug.apk`.
9. Tap `app-debug.apk`. If Android asks, allow Chrome or your file manager to **Install unknown apps**, then install it.

## Notes

- The APK is a debug-signed installable test build. It is suitable for personal installation. A Play Store release should use a private release keystore and a signed release build.
- Keep the same GitHub repository for future updates. Upload changed source files and rerun the workflow.
- This app requires internet access. Website login, database, permissions, and business logic remain controlled by the website.
- File selection and downloads are enabled. External web links open in the phone's browser. Only the exact website host is kept inside the app.
- The website could not be inspected for its internal implementation through the available page reader. Please test login, stock entry, file upload/download, and any camera or barcode features after installing. If the site uses additional subdomains for login or APIs, those may need to be added to the in-app host allowlist.
