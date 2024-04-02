# WebAR
This project is WebAR Image Tracking, developed in Android Studio - Instant App, the original code is Java, I change the code into kotlin, ATTENTION: This is Kotlin Project.

**But need someone to clean the code a bit to get a better version.

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


