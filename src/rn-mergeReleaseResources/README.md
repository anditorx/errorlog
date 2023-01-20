# React Native Android Build FAILD :app:mergeReleaseResources | Duplicate Resource

Build React native error **mergeReleaseResources**


### Android

Add code in **node_modules/react-native/react.gradle.** After **doFirst**
```js
doLast {
	def moveFunc = { resSuffix ->
		File originalDir = file("$buildDir/generated/res/react/release/${resSuffix}");
		if (originalDir.exists()) {
			File destDir = file("$buildDir/../src/main/res/${resSuffix}");
			ant.move(file: originalDir, tofile: destDir);
		}
	}
	moveFunc.curry("drawable-ldpi").call()
	moveFunc.curry("drawable-mdpi").call()
	moveFunc.curry("drawable-hdpi").call()
	moveFunc.curry("drawable-xhdpi").call()
	moveFunc.curry("drawable-xxhdpi").call()
	moveFunc.curry("drawable-xxxhdpi").call()
		moveFunc.curry("raw").call()
}
```

### OR
- `cd android && ./gradlew clean`
- Open **build.gradle** --> **android/app/build.gradle**
- comment this line
```js
//apply from: "../../node_modules/react-native/react.gradle"
```
Source: [Duplicate Resource](https://github.com/facebook/react-native/issues/26245)
