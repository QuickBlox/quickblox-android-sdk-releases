# QuickBlox Android Releases
This repository contains binary distributions of [QuickBlox](https://quickblox.com) Android SDK.

# Overview
This repository contains releases of the Android SDK for interacting with the QuickBlox communications cloud.

QuickBlox  is Communication as a Service provider. The platform provides chat using the XMPP protocol, WebRTC signalling for video/voice calling and an API for sending push notifications. It provides a user management system, data storage and more. 

[Project page on QuickBlox developers section](http://quickblox.com/developers/Android)

## Installation

The QuickBlox Android SDK can be installed directly into your application by importing a JAR from the filesystem or an JAR/AAR via Maven.

### Maven Installation

The recommended path for installation on Android is via [Maven](http://maven.apache.org/). Maven is a software project management and comprehension tool. It is capable of managing a project's build configuration and dependencies from a central location. You can install the QuickBlox SDK into your project via Maven by adding the following code to your project's `build.gradle` file:

```groovy
allprojects {
    repositories {
        maven {
            url "https://github.com/QuickBlox/quickblox-android-sdk-releases/raw/master/"
        }
        mavenCentral()
    }
}

def qbSdkVersion = '2.5'

dependencies {
    // online dependencies, from remote repository, aar files
    //
    сompile "com.quickblox:quickblox-android-sdk-core:$qbSdkVersion@aar"
    сompile ("com.quickblox:quickblox-android-sdk-chat:$qbSdkVersion@aar"){
        transitive=true
    }
    сompile "com.quickblox:quickblox-android-sdk-content:$qbSdkVersion@aar"
    сompile "com.quickblox:quickblox-android-sdk-messages:$qbSdkVersion@aar"
    сompile "com.quickblox:quickblox-android-sdk-customobjects:$qbSdkVersion@aar"
    сompile "com.quickblox:quickblox-android-sdk-location:$qbSdkVersion@aar"
    сompile "com.quickblox:quickblox-android-sdk-videochat-webrtc:$qbSdkVersion@aar"
}
```

### JAR Installation

To install the QuickBlox Android SDK directly from a JAR binary download the latest JAR release from the Github project and complete the following steps:

1. Drag the JAR file into the /libs directory of your Android Studio application Navigate to the JAR file in Android Studio navigatior, right click and select "Add As A Library..."
2. Navigate to your build.gradle file and ensure that you include the following:

```groovy
dependencies {
    compile fileTree(dir: 'libs', include: ['*.jar'])
}
```

## Questions and feedback

Please raise questions, requests for help etc. via http://stackoverflow.com/questions/tagged/quickblox
