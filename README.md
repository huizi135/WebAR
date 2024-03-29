# WebAR
This project is WebAR Image Tracking, developed in Android Studio - Instant App, the original code is Java, I change the code into kotlin, ATTENTION: This is Kotlin Project.

But need someone to clean the code a bit to get a better version.

## Here I add few steps have been done.
- Enable AR Core
- Add Image Tracking Feature
- Enable Instant App
- Create App Link (ongoing)

### Enable AR Core
## 1. Enable AR Core

To make your app AR Required or AR Optional, update your AndroidManifest.xml to include the following entries:
```kotlin


@@ -64,5 +64,25 @@ dependencies {

```

## 2. Add Image Tracking Feature

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
