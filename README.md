Pos Printer Demo Android project
================================

What this contains
- Simple Android app with a UI to enter printer IP:port and do a test print over TCP (port 9100).
- Implements RawTcpPrinter, EscPos helpers, bitmap->raster conversion, QR generator.

How to build APK (locally)
1. Install Android Studio and SDK (recommended).
2. Open the folder pos_printer_app in Android Studio (open settings.gradle.kts).
3. Let Gradle sync. If Kotlin/Gradle plugin versions differ, update versions in build files.
4. Connect an Android device or use emulator (emulator should have network access to printer IP).
5. Build > Build Bundle(s) / APK(s) > Build APK(s).
6. Install the APK on device and run.

Notes
- Place a `logo.png` in app/src/main/assets/ if you want logo printing.
- This environment cannot build the APK for you; the project is ready to build locally.


Added features:
- Room DB (Product, Cart, Transactions)
- Cashier UI (product list, cart, payment)
- Payment activity with printing and recording transaction
- Open drawer command via raw TCP (uses ESC/POS DRAWER command)

Build as before in Android Studio.


Additional features added:
- Bluetooth printer adapter (BluetoothPrinter.kt)
- USB OTG printer adapter placeholder (UsbPrinter.kt)
- PrinterManager to manage printers, enqueue jobs, and support kitchen mode (no-cut)
- SettingsActivity to toggle Auto-Cut and Kitchen Mode and save printer IP/port

Notes:
- USB printing often requires vendor-specific handling; UsbPrinter.kt is a template placeholder.
- For Bluetooth printing, the app requires BLUETOOTH_CONNECT (Android 12+) runtime permission; add permission handling when targeting API 31+.
- Cloud sync (Firebase) and Google Drive backup can be integrated; I left a CloudSync interface placeholder if you want I can wire Firebase next.
\nFinal notes: To enable Firebase and Google Drive features you must configure Firebase project and Google OAuth credentials as described above. After placing google-services.json in app/ and configuring OAuth clients, reopen the project in Android Studio and sync.\n