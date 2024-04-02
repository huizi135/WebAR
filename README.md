# WebAR
This project is WebAR Image Tracking, developed in Android Studio - Instant App, the original code is Java, some are kotlin.

## Here I add few steps have been done.
- Enable AR Core
- Add Image Tracking Feature
- Enable Instant App
- Create App Link (ongoing)

### Enable AR Core

To make your app AR Required or AR Optional, update your AndroidManifest.xml to include the following entries:
```kotlin
<uses-permission android:name="android.permission.CAMERA" />

<!-- Limits app visibility in the Google Play Store to ARCore supported devices
     (https://developers.google.com/ar/devices). -->
<uses-feature android:name="android.hardware.camera.ar" />

<application …>
    …

    <!-- "AR Required" app, requires "Google Play Services for AR" (ARCore)
         to be installed, as the app does not include any non-AR features. -->
    <meta-data android:name="com.google.ar.core" android:value="required" />
</application>
```
Then, modify your app's build.gradle to specify a minSdkVersion of at least 24:
```kotlin
 android {
     defaultConfig {
         …
         minSdkVersion 24
     }
 }
```
Add build dependencies
To add ARCore to your Android Studio project, do the following:

Make sure your project's build.gradle file includes Google's Maven repository.
```kotlin
allprojects {
    repositories {
        google()
        …
    }
}
```

Add the latest ARCore library as a dependency in your app's build.gradle file.
```kotlin
dependencies {
    …
    implementation 'com.google.ar:core:1.33.0'
}
```
[for more information, Check if ARCore is supported, if Google Play Services for AR is installed, Request camera permission](https://developers.google.com/ar/develop/java/enable-arcore)

## 2. Add Image Tracking Feature


## 3. Enable Instant App

#### Enabke Instant App Development 
Tools -- SDK Manager -- System Settings -- Android SDK -- SDK Tools -- INSTALL Google Play Instant Development SDK 
![image](https://github.com/huizi135/WebAR/assets/91324319/994c8840-93a0-45c9-9150-b12b944ea88a)

#### APP Folder, right click, Refactor -- Enable Instant App Support
![image](https://github.com/huizi135/WebAR/assets/91324319/dafc134c-a83c-4844-af3a-0eb7c76f529b)

After enable instant app support, you will find those below in your AndroidManifest
![image](https://github.com/huizi135/WebAR/assets/91324319/5941fef0-034a-4d40-b356-cebe9e974656)
This is configure the module - Instant App to true

#### Before launch your app, go to Edit - App Configuration - apply Deoply as Instant App - ok 
![image](https://github.com/huizi135/WebAR/assets/91324319/ab9e9cc8-8e66-4d16-ae2e-d3e90c8c2696)

Now you can test your project as Instant App

Attention: use a real mobile or tablet as WebAR test device¦
