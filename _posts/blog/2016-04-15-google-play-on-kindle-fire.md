---
published: true
categories: 
  - blog
---
## Google Play on Kindle Fire

Want to set up Google Play on Kindle Fire so apps can be installed from Play Store, read books on Google Play books etc.

I did all of this on Windows 7 PC. XDA forums posts were very helpful (http://forum.xda-developers.com/amazon-fire/general/installing-google-framework-playstore-t3216122/post63101324#post63101324)

I created a file under C:/Users/{adminaccount}/.android/adb_usb.ini containing the following line:

`0x1949`

(There was already an equivalent file in C:/Users/{mynormalusername}/.android/adb_usb.ini, need to have one under the admin user though).

Need to install Amazon drivers - https://developer.amazon.com/public/resources/development-tools/ide-tools/tech-docs/05-setting-up-your-kindle-fire-tablet-for-testing (kindle_fire_usb_driver.zip)

In C:/Users/{mynormalusername}/AppData/Local/Android/android-sdk/platform-tools, ran:

N.B. I also added the above path to the Path environment variable

adb devices

Then ran:

adb shell pm grant com.google.android.gms android.permission.INTERACT_ACROSS_USERS

Downloaded Amazon-Fire-5th-Gen-Install-Play-Store.zip from http://rootjunkysdl.com/files/?dir=Amazon%20Fire%205th%20gen

## To remove ads form lock screen, I had to root device

- Downloaded AmazonFire5thGenSuperTool.zip from rootjunky: http://rootjunkysdl.com/files/?dir=Amazon%20Fire%205th%20gen/SuperTool

- Unzipped .zip file and had to edit 1-Amazon-Fire-5th-gen.bat file - needed to remove files\ before adb.exe etc. on each line (did a search and replace in Sublime)

- Follow steps to install Kingroot, then supersu.

- Removed Kingroot

- Ran bat file again and selected option 3 to disable OTA updates from Amazon

- Removed supersu

## Kindle Fire went into a reboot loop when on wifi - guess Amazon was trying to push an update (despite me having tried to disable OTA updates).

- Had trouble getting Fire to be recognised when plugged into Windows PC in recovery mode. Wasn't able to follow restore/unroot a rooted Kindle fire YouTube video from Rootjunky.

- Decided to just put Kindle Fire into recovery mode, then selected restore factory defaults. **Luckily**, this worked. Ads are still gone - but it's no longer rooted and I don't have Google Play store installed. Not really a big deal - I think I'll leave it this way.
