# React Native Android: Static Image is not showing in production released apk

This command work for me
```bash
  react-native bundle --platform android --dev false --entry-file index.android.js \ --bundle-output android/app/src/main/assets/index.android.bundle \ --assets-dest android/app/src/main/res/
```

Source: [Static Image is not showing](https://stackoverflow.com/questions/38941436/react-native-android-static-image-is-not-showing-in-production-released-apk)
