# APK build

The web app changes are complete and an Android WebView wrapper is included under `android/`.

Before building, set `app_url` in `android/app/src/main/res/values/strings.xml` to the deployed HTTPS Lorekeep URL. The URL must serve the web app's server routes because story generation uses `/api/story` and `/api/memory`.

Then run from the repository root:

```bash
gradle -p android assembleDebug
```

The APK is written to `android/app/build/outputs/apk/debug/app-debug.apk`.

A GitHub Actions workflow at `.github/workflows/android-apk.yml` can build the APK in CI as well.
