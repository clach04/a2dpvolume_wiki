Starting in version 2.12.2 the old accessibility method for reading notifications was replaced with the new notification listener service introduced in Android 4.3  This service works differently than the old accessibility service.

Once you install A2DP Volume, go to your Android settings.  Select [sound & notification] -> [notification access].  Then find A2DP Volume in the list of apps.  It may be the only one listed.  Check the box next to A2DP Volume.  Accept the dialog box that pops up.  Now you should be set.  Of course you also need to enable reading notification messages in the preferences of A2DP Volume, and again enable reading text messages in each device in A2DP Volume.  

This feature uses the same apps list as the old accessibility feature did.  This means you need to select the menu in A2DP Volume (dots on top right), then [apps for accessibility].  Check all the apps you want notifications read for.  

## Set up A2DP Volume and devices 
After you install A2DP volume and get all your devices set up, make sure you enable "Enable reading notification messages" in the preferences menu of A2DP Volume.  

![](http://jimroal.com/A2DPScreens/preferences2b.png)

The screen above shows both "enable reading text messages" and "enable reading notification messages" checked. This can result in messages being read twice. Normally if you want to read both SMS and other notifications, you would just use the "enable reading notification messages" and depend on the SMS notification to be read.  The old SMS reader directly reads the SMS message.  The newer notification reader uses a notification listener to read the notifications.  

Back out of the preferences with the Android back button so they take effect.  Now go to each device and check the "enable reading text messages?" checkbox.

![](http://jimroal.com/A2DPScreens/EditDevice1b.png)

Do this for each device that you want to have messages read while connected.  Devices are listed in the main A2DP Volume screen. Bluetooth devices must first be paired and the "find devices" button in A2DP Volume run to list the devices.  Click a device name and select "edit" to configure settings for that device.

## Set up the apps for accessibility in A2DP Volume 

Now click on the preferences button while in the A2DP Volume main screen.  Click on "apps for accessibility" in the menu.

![](http://jimroal.com/A2DPScreens/A2DPVolume8.png)

You will see a list of all the apps installed on the device.  This includes system apps as well as downloaded apps and other packages.  

![](http://jimroal.com/A2DPScreens/accessibilityapps.png)

Check the box next to the apps of your choice.  Be careful not to have silly things happen such as checking A2DP Volume itself or car mode. These can cause infinite loops.


