# Deagle

Deagle library for Android

## For Pixel 9 Pro Fold Users

You can download the pre-built library (AAR file) without building it locally:

1. Go to the [Actions tab](https://github.com/CurrenlyDying/deagle/actions/workflows/build-library.yml) in this repository
2. Click on the latest successful workflow run
3. Scroll down to the "Artifacts" section
4. Download the `deagle-library` artifact
5. Extract the ZIP file to get the AAR file

The library is automatically built using GitHub Actions whenever code is pushed to the `main` or `dev` branches. The workflow:
- Uses Android SDK 34 for modern device compatibility (including Pixel 9 Pro Fold)
- Produces a release-optimized AAR file
- Artifacts are retained for 90 days

## Using the AAR in Your Project

1. Place the AAR file in your app's `libs` folder
2. Add the following to your app's `build.gradle`:

```gradle
dependencies {
    implementation files('libs/library-release.aar')
}
```

## Building Locally (Optional)

If you prefer to build the library yourself:

```bash
./gradlew :library:assembleRelease
```

The AAR will be located at `library/build/outputs/aar/library-release.aar`

## Requirements

- **Min SDK**: 21 (Android 5.0)
- **Target SDK**: 34 (Android 14)
- **Compile SDK**: 34

## License

See [LICENSE.txt](LICENSE.txt)
