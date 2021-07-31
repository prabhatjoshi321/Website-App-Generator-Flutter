# Website App Generator

This project utilises flutter to output **cross platform apps** that can be uploaded both on **Playstore** as well as **Apple's appstore**. This solution only works with respondive apps and websites having SSL.

## Features

* Custom Splash Screen and Icons
* Back history cache
* Redirect to app on app specific links.
* Similar to other apps with no compromise on performance.

## Prerequisires

* [Vscode](https://code.visualstudio.com/download) needs to be installed together with [Complete Flutter Extension Pack](https://marketplace.visualstudio.com/items?itemName=GulajavaMinistudio.complete-flutter-extension-pack)
* [Flutter sdk](https://flutter.dev/docs/get-started/install) needs to be installed and added to system path.

## How to use

* Go to [assets/images](./assets/images/) folder and replace the **icon** and **splash screen** with your desired ones.(Keep the filenames and image format same)
* Open Vscode in the project's directory.
* Goto **Find All** by pressing **Ctrl+shift+F** and search for **com.generate.webapp**. Replace all occurrences with your desired package name.(eg. com.appname.webapp)
* Navigate to **android\app\src\main\kotlin\com** [here](./android/app/src/main/kotlin/com/) and rename **generate** folder with your **App's Name**.
* Navigate to **android\app\src\main\AndroidManifest.xml** [here](./android/app/src/main/AndroidManifest.xml), On **line 11** change **generate** with your app's name.
* Now the difficult part is done. Here the steps change for **IOS** and **Android**.

### **Steps for Android**

* Open a vscode terminal and execute following commands
  * flutter pub get
  * flutter pub run flutter_launcher_icons:main
  * flutter build apk --release
* App is ready. Navigate to **build\app\outputs\flutter-apk\app-release.apk** [here](./build/app/outputs/flutter-apk/app-release.apk), This is your app in apk format. Upload it on playstore.
* Refer [here](https://flutter.dev/docs/deployment/android) if you face any difficulties.

### **Steps for IOS**

* For IOS, follow [this](https://flutter.dev/docs/deployment/ios) guide for deploying it on appstore
