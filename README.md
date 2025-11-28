POS Printer Android (Classic UI skeleton)

This project is a simplified POS app skeleton (Classic UI style) ready to be built by GitHub Actions.
- It includes a basic app module and a simple RawTcpPrinter ESC/POS helper.
- To build on GitHub Actions we use system Gradle (no wrapper required).

Build:
- Upload this project as-is to your GitHub repository (upload the files, not a ZIP).
- Make sure Actions workflow `.github/workflows/android.yml` is present (included).
- Push to main branch, Actions will run and produce `app-debug.apk` as artifact.

Notes:
- For Firebase/Drive features you must add google-services.json and configure OAuth.
- This skeleton focuses on getting an APK buildable quickly; you can extend with the full modules later.
