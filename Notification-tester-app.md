I copied the LNotifications sample app and added the ability to invoke car mode for testing.  It is rough but can be useful.  Download the APK here: https://drive.google.com/file/d/0B2ZRdduGQB59X1kwTEotVXI3cVU

The way I use it is open the LNotifications app and invoke car mode.  Then you can use car mode in A2DP Volume to set up actions such as reading notifications.  This will put A2DP Volume in connected more with car mode settings.

When you invoke car mode your device will change the homescreen UI to the car mode homescreen.  Some devices don't have one so if you try to go home you will get strange behavior.  Use the recent apps button in Android (the right boxes) to navigate back to the LNotificationsSample app and toggle the car mode button to get back out of car mode.  

It supports many notification types.  You can read the documentation in the Android samples for LNotifications sample.  

It now has a notifications reader feature that will read all notifications and create a text file in the sd card NotCatch folder.  If you enable it to read notifications in Android settings, it will read them all and make files.  DON'T leave it enabled!  The intent is to enable it and capture some notifications to see what fields they are populating.  Then disable it in the Android settings to stop it.  It is very rough and not at all production worthy.  

This app is only useful for testing.  It is rough so don't expect great things.  Here is the sample app I modified: https://developer.android.com/samples/LNotifications/index.html  