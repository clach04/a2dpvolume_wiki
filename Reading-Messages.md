#How to get the text and notifications message reader working.

## A2DP Volume and TTS

Note: This app has not yet implemented changes for Android 5.0 to get this working again.  See details here: https://github.com/jroal/a2dpvolume/issues/197

A2DP Volume can use any text-to-speech (TTS) engine for reading text messages (SMS) and Google Talk messages.  This requires several things to work:

* You must have a TTS engine installed.  Some common ones are Pico and eSpeak.  I use Google or Pico and have good results.
* Don't select "silence notifications" on the device you also want to hear notifications on.  The silence setting will stop the notifications.
* Make sure no other app is silencing notifications.
* Sony and some LG devices have broken the TTS engine.  I can't fix this.  When A2DP Volume tries to make the TTS data check on these devices A2DP Volume may crash because Sony and LG have removed the Android package that I need to call so it gets a null pointer exception.  Thank you Sony and LG.  Documentation of this issue is here http://stackoverflow.com/questions/25830230/android-text-to-speech-throws-activitynotfoundexception.
* That TTS engine must be initialized and have downloaded the latest speech data.  This happens automatically in most cases.  You can test for this in Android by going to [menu button] then [voice input and output settings].  Click on text-to-speech settings.  At the top click [listen to example].  If this does not work, A2DP Volume won't either.
* You must have a default TTS engine selected.  If you have more than one TTS engine installed, and you don't have a default selected, it will pop up a dialog asking you for which one to use rather than actually reading anything.
* You must enable reading text messages in A2DP Volume.  This is done by checking this box in the preferences in A2DP Volume. 
![](http://jimroal.com/A2DPScreens/A2DPVolume7.png)

* You must ALSO select read text messages for each device.  This is done by selecting the device in the list and clicking edit in the popup dialog.
![](http://jimroal.com/A2DPScreens/editdevice1b.png)

* You must select a valid stream (music stream selected above).  This is done at the bottom of the preferences menu.  It is called SMS stream.  Depending on your devices, some may not work at all so you will need to try all 3 until you find the one that works best.  You can select the stream in the edit device screen.  Click a device in your list and then click edit when the dialog pops up.
* In the devices you would like TTS to read messages, you need to enable it in the edit device screen.  Make sure you save when done editing!  The save button is at the bottom of this screen.
* **Note: You must have TTS enabled in BOTH the preferences and EACH of the devices you want to read text messages while connected.**

## If it still does not work
 * Reboot your device. Sometimes the accessibility settings don't take effect until after a boot.
 * If you use Handscent: Handscent => Settings => Application Settings => Default Messaging Application = Disable.  See comment below.  If you have other apps installed that intercept SMS they may have a similar issue.
 * Make sure you are watching the Android device screen while trying to read the first text.  If any dialogs pop up, make sure you select a default before clicking OK.    It is common for more than one TTS engine to be installed on your device and if a default is not selected, it will just sit and wait until you select one.  Obviously, don't try this while driving!  Make sure you get it working before you drive anywhere.
 * Make sure you have a default TTS engine selected and working.
 * Go into [manage applications] in Android.  Select your TTS engines and clear defaults.  Then test the TTS engine again as described above.  You will need to select a default again.
 * Different devices work with different streams.  Try each of the TTS streams to see which one if any work for you.  This is a configuration in each device in A2DP Volume. Generally A2DP devices use the music stream.  If your device also supports hands free calling you can use the voice call stream.  Try each one.  Make sure to stop and restart the service when you change this configuration. 
 * For reading notification make sure you set up the notification settings: https://github.com/jroal/a2dpvolume/wiki/Notification-Reader-Settings .  If using A2DP Volume 2.11 or older you need to set up the accessibility settings: https://github.com/jroal/a2dpvolume/wiki/Accessibility-Settings
 * If all else fails, uninstall and reinstall A2DP Volume

## If you have any helpful information... 
... please post to this wiki.  Your information can be valuable to others.  I only have Motorola phones and a Lenovo tablet to develop on.  I also use the emulator of course.  My only Bluetooth devices are Motorola T605, Mercedes sedan, and a Monoprice A2DP receiver. There are hundreds of other devices out there.  If you have found ways to get it working please let others know here.  Thanks.

Note: Don't comment here if you think you fund a bug or need a reply to a question.  If you have a question email.  If it is a defect, report it on the https://github.com/jroal/a2dpvolume/issues issues list.

Accessing the edit device screen:
This screen shows the result from a short press on a device in the list.  Here you can select to edit this device or delete this device from the list.  The OK button just returns you to the app main screen.

![](http://jimroal.com/A2DPScreens/Image2.png)

The screen below shows where to set the enable reading text messages.  When you check that box, more dialog will appear below as shown.  There you can set the delay and the stream.

![](http://jimroal.com/A2DPScreens/EditDevice3.png)