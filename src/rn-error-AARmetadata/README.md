# React Native Run Android ERROR: AAR metadata


Change **sdkVersion** in `android/build.gradle`
```java
compileSdkVersion = 31
targetSdkVersion = 31
```
then
```java
allprojects {
    repositories {
        mavenCentral()
        mavenLocal()
        maven {
            // All of React Native (JS, Obj-C sources, Android binaries) is installed from npm
            url("$rootDir/../node_modules/react-native/android")
        }
        maven {
            // Android JSC is installed from npm
            url("$rootDir/../node_modules/jsc-android/dist")
        }

        google()
        jcenter()
        maven { url 'https://www.jitpack.io' }

				// ------ tambahkan kode dibawah ini -----//
        exclusiveContent {
           // We get React Native's Android binaries exclusively through npm,
           // from a local Maven repo inside node_modules/react-native/.
           // (The use of exclusiveContent prevents looking elsewhere like Maven Central
           // and potentially getting a wrong version.)
           filter {
               includeGroup "com.facebook.react"
           }
           forRepository {
               maven {
                   // NOTE: if you are in a monorepo, you may have "$rootDir/../../../node_modules/react-native/android"
                   url "$rootDir/../node_modules/react-native/android"
               }
           }
       }

			// --------- //

    }
}
```

Source: 
- [Debug AAR Metadata](https://stackoverflow.com/questions/68221505/task-appcheckdebugaarmetadata-failed-when-run-react-native-run-android)
- [Compile debug kotlin](https://stackoverflow.com/questions/72346334/execution-failed-for-task-react-native-webviewcompiledebugkotlin)
