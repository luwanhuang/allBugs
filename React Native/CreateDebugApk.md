## Create Debug Apk
### 1. clear the file  
go to 
`android/app/src/main/assets/index.android.bundle`  
if no file and no folder, create it.  
if it has, delete all content in the file.
### 2. input follow command
`
react-native bundle --platform android --dev false --entry-file index.js --bundle-output android/app/src/main/assets/index.android.bundle --assets-dest android/app/src/main/res/
`  
### and
`
cd android && ./gradlew assembleDebug
`  
then you can find apk at
`app/build/outputs/apk/debug/app-debug.apk`

