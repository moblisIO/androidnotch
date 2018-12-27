# Cordova Android Cutout Plugin

Detect cutout (aka notch) on Android devices.
Returns true if cutout/notch is detected on Android device.  
Note: Requires SDK target API 28+ (Pie).

## Using

Create a new Cordova Project & Android Platform

    $ cordova create testApp 
    $ cd testApp
    $ cordova platform add android
    
Install the plugin

    $ cordova plugin add https://github.com/moblisIO/androidcutout.git    

Edit `www/js/index.js` and add the following code inside `onDeviceReady`

```
var success = function(hasCutout) {
    if (hasCutout){
        alert('has cutout');
    }else{
        alert('no cutout')
    }
}

var failure = function(e) {
    alert("Error calling Cutout Plugin");
}

cutout.hasCutout(success, failure);

```

Install on Android platform

    $ cordova platform add android
    

## Note

Android Studio project structure must be set to Compile Sdk Version API 28 (Pie)+.
1. Build Cordova project on the command line first
    a. $ cordova build android
1. Open Android Studio
2. Open an Existing Android Studio Project
3. Select No if asekd to upgrade project
4. Select "app" in the Project tab
5. Select "File/Project Structure"
6. Select app under "Modules"
7. Select API 28 under Compile Sdk Version


Run the code

    $ cordova run android

    or

    $ cordova emulate android
