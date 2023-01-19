# React Native - ERROR ':app:mergeDexDebug'

At Path `android/app/build.gradle`

```bash
defaultConfig {
	multiDexEnabled true //Add this line
}

dependencies{

	...
	implementation 'androidx.multidex:multidex:2.0.1'
	...
}
```
