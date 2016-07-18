Starting in version 2.12.2 the old accessibility method for reading notifications was replaced with the new notification listener service introduced in Android 4.3  This service works differently than the old accessibility service.

Once you install A2DP Volume, go to your Android settings.  Select [sound & notification] -> [notification access].  Then find A2DP Volume in the list of apps.  It may be the only one listed.  Check the box next to A2DP Volume.  Accept the dialog box that pops up.  Now you should be set.  Of course you also need to enable reading notification messages in the preferences of A2DP Volume, and again enable reading text messages in each device in A2DP Volume.  

This feature uses the same apps list as the old accessibility feature did.  This means you need to select the menu in A2DP Volume (dots on top right), then [apps for notifications].  Check all the apps you want notifications read for.  

Notification have become more complex.  Apps have significant flexibility on how they use them. A2DP Volume attempts to parse out the most useful bits.  Android made a field just for apps that want to read out the useful bit.  This field is called "tickerText".  A2DP volume looks for that field to be populated first.  If it's not, it looks for several other fields.  It then combines this info to read out.  Results will vary!  Some apps just don't work right at all so reading their messages will not be good.  A2DP Volume also attempts to prevent the same message reading multiple times.  However, this too is a challenge.  I tested with Hangouts primarily.  Gmail will read out only the sender and subject. I also tested with Skype.

## Set up A2DP Volume and devices 
After you install A2DP volume and get all your devices set up, make sure you enable "Enable reading notification messages" in the preferences menu of A2DP Volume.  

![](http://jimroal.com/A2DPScreens/preferences2b.png)

The screen above shows both "enable reading text messages" and "enable reading notification messages" checked. This can result in messages being read twice if you were to also select your SMS app in the "apps for notifications" menu. If you use an app like Hangouts or Facebook Messenger for SMS and want both the SMS and other messages read, use the notification reader only and uncheck "enable reading text messages" above.

Back out of the preferences with the Android back button so they take effect.  Now go to each device and check the "enable reading text messages?" checkbox.  In the device specific settings, "enable reading text messages" actually enables the reading of any messages. The app preferences defines what messages could be read and device specific settings allows them to be read or not.  

![](http://jimroal.com/A2DPScreens/EditDevice1b.png)

Do this for each device that you want to have messages read while connected.  Devices are listed in the main A2DP Volume screen. Bluetooth devices must first be paired and the "find devices" button in A2DP Volume run to list the devices.  Click a device name and select "edit" to configure settings for that device.

## Set up the apps for notifications in A2DP Volume 

Now click on the preferences button while in the A2DP Volume main screen.  Click on "apps for notifications" in the menu. Note: this was previously called "apps for accessibility".

![](http://jimroal.com/A2DPScreens/A2DPVolume8.png)

You will see a list of all the apps installed on the device.  This includes system apps as well as downloaded apps and other packages.  

![](http://jimroal.com/A2DPScreens/accessibilityapps.png)

Check the box next to the apps of your choice.  Be careful not to have silly things happen such as checking A2DP Volume itself or car mode. These can cause infinite loops.


## Android settings to enable notification reading

Below is how you enable A2DP Volume to read notifications in Android settings.  A Nexus device is shown.  Other devices may have different settings menus.  

Select "Sound & Notification" from this menu.
![](http://jimroal.com/A2DPScreens/NotSettings1.png)

Select "Notification Access" from this menu.
![](http://jimroal.com/A2DPScreens/NotSettings2.png)

Check the box next to A2DP Volume to allow A2DP Volume to access the notifications which is required to enable reading them.
![](http://jimroal.com/A2DPScreens/NotSettings3.png)
