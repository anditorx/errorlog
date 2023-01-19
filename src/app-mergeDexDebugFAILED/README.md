# React Native Error: Task :app:mergeDexDebug FAILED

Android 5.0 (API level 21) and higher uses ART which supports multidexing. Therefore, if your minSdkVersion is 21 or higher, the multidex support library is not needed.

Modify At Path android/app/build.gradle

```bash
android {
  compileSdkVersion 22
  buildToolsVersion "23.0.0"
  defaultConfig {
      minSdkVersion 14 //lower than 14 doesn't support multidex
      targetSdkVersion 22

      // Enabling multidex support.
      multiDexEnabled true
  }
}

dependencies {
  implementation 'com.android.support:multidex:1.0.3'
}
```

[Source](https://github.com/react-native-webview/react-native-webview/issues/1344)
