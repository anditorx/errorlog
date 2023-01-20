# Cocoapod - Error cocoapods pod install M1

Get error while trying `pod install`

Try this command in `[YOUR-PROJECT]/ios`
```bash
  sudo arch -x86_64 gem install ffi
```
Then
```bash
  arch -x86_64 pod install
```
OR
```bash
  arch -x86_64 pod install --repo-update
```

Source: [Error cocoapod install in m1](https://github.com/CocoaPods/CocoaPods/issues/10220#issuecomment-730963835)
