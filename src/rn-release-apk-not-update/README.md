# React Native - Release APK Not Updating in React Native

Gradlew assembleRelease not updating APK output file

Android
```bash
  react-native bundle --platform android --dev false --entry-file index.js --bundle-output android/app/src/main/assets/index.android.bundle --assets-dest android/app/src/main/res
```

IOS
```bash
  react-native bundle --dev true --assets-dest ./ios --entry-file index.js --platform ios --bundle-output ios/main.jsbundle
```

Source: [Release apk not update](https://stackoverflow.com/questions/45441217/release-apk-not-updating-with-javascript-code)
