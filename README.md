# ChronoFlow Stopwatch (Kotlin Android)

A native Android stopwatch starter project with a premium dark interface.

## Features
- Start, pause, resume, lap and stop controls
- Centisecond display using Android's monotonic elapsed realtime clock
- Lap split list, lap quantity and average lap split
- Session naming and locally persisted history
- Export a selected saved session as a PDF using Android's document picker
- Hardware volume key shortcuts while the app is open:
  - Volume Up: Start/Resume; while running, Pause
  - Volume Down: Add Lap
  - Hold Volume Down: Stop and open the save dialog
- GitHub Actions workflow builds a debug APK automatically

## Build on GitHub
1. Create a new GitHub repository.
2. Upload the contents of this folder (the `app`, `.github`, and Gradle files) to the repository root.
3. Open **Actions** and run **Build Android APK**, or push to `main`/`master`.
4. Open the completed workflow run and download the `ChronoFlow-debug-apk` artifact.

## Build locally
Open this folder in Android Studio (JDK 17; Android SDK 35 installed), allow Gradle sync, then choose **Build > Build Bundle(s) / APK(s) > Build APK(s)**.

## Notes
- Hardware volume shortcuts work while ChronoFlow is the foreground app. Android does not allow a normal app to capture volume keys while another app is in front.
- The timer uses `SystemClock.elapsedRealtime()` so it is not affected by changes to the device clock.
- Session history is stored locally on the device. No account or internet permission is required.
- Package/application ID: `com.chronoflow.stopwatch`.
