---
published: true
categories: 
  - blog
---
## Google Play on Kindle Fire

Want to set up Google Play on Kindle Fire so apps can be installed from Play Store, read books on Google Play books etc.

I did all of this on Windows 7 PC. XDA forums posts were very helpful.

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