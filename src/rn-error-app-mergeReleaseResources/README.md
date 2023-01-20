# React native Execution failed for task ':app:mergeReleaseResources'

Here is the simple solution :
- Delete build inside **android/app** folder
- Delete build inside **android** folder
- run `rm -rf $HOME/.gradle/caches/`
- Open **build.gradle --> android/app/build.gradle**
- comment this line
```js
  //apply from: "../../node_modules/react-native/react.gradle"
```
- Delete **index.android.bundle** file from assets folder and re-create using **react-native bundle --platform android --dev false --entry-file index.js --bundle-output android/app/src/main/assets/index.android.bundle --assets-dest android/app/src/main/res**
- run `react-native run-android` Or `run react-native run-android --variant=release`


Source: [React Native Android Duplicate Resource](https://stackoverflow.com/questions/52632950/react-native-0-57-1-android-duplicate-resources/55245362#55245362)
