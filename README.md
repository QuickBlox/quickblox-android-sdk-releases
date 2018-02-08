# QuickBlox Android Releases
This repository contains binary distributions of [QuickBlox](https://quickblox.com) Android SDK.

# Overview
This repository contains releases of the Android SDK for interacting with the QuickBlox communications cloud.

QuickBlox  is Communication as a Service provider. The platform provides chat using the XMPP protocol, WebRTC signalling for video/voice calling and an API for sending push notifications. It provides a user management system, data storage and more. 

[Project page on QuickBlox developers section](http://quickblox.com/developers/Android)

## Installation

The QuickBlox Android SDK can be installed directly into your application by importing sdk artifacts via Gradle.

### GRADLE Installation
Add the following code to your **project's** `build.gradle` file:

```groovy
allprojects {
    repositories {
        maven {
            url "https://github.com/QuickBlox/quickblox-android-sdk-releases/raw/master/"
        }
    }
}

def qbSdkVersion = '3.7.0'

```
And the following code to your **module's** `build.gradle` file:
```groovy

dependencies {
    //
    сompile "com.quickblox:quickblox-android-sdk-chat:$rootProject.qbSdkVersion" //include only necessary module dependency, all transitive modules will be included automatically
    сompile "com.quickblox:quickblox-android-sdk-content:$rootProject.qbSdkVersion"
    сompile "com.quickblox:quickblox-android-sdk-messages:$rootProject.qbSdkVersion"
    сompile "com.quickblox:quickblox-android-sdk-customobjects:$rootProject.qbSdkVersion"
}
```

## Questions and feedback

Please raise questions, requests for help etc. via http://stackoverflow.com/questions/tagged/quickblox
