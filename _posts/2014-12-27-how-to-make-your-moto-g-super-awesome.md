---
title: How To Make your Moto G super awesome!
date: 2014-12-27T10:07:44+00:00
author: Redgadget
layout: post
permalink: /how-to-make-your-moto-g-super-awesome/
categories:
  - Hack
  - Technology
tags:
  - Hack
  - Moto G
  - Root moto g
img: navbar.jpg
---
Installing a custom ROM on your Moto G could be a tedious process. But there is an easier solution for this! You can have all those features of a **custom ROM** in your **stock ROM** without any hassle ( a little hassle) by installing **Xposed Framework**.


## <span id="Steps_in_brief">Steps in brief</span>

> Our main goal is to install Xposed Framework on your device.
> 
> [What is Xposed Framework?](http://www.xda-developers.com/android/android-basics-101-understanding-xposed-framework-xda-developer-tv/)

  * Backup all your data (may be on your PC) because unlocking the bootloader on a Motorola device will automatically wipe all device data
  * Root your phone (Unlocking the device)
  * Install Recovery
  * Install Xposed Framework
  * Install GravityBox

That&#8217;s all!

Read: <a href="http://redgadgets.com/why-should-i-root-my-moto-g/" target="_blank">Why should I root my Moto G?</a>

# <span id="Rooting">Rooting</span>

## <span id="Step_1_Take_deep_breaths">Step 1: Take deep breaths!</span>

Yes you are rooting your Moto G. Your warranty will be void. Your phone could just be months old and you are afraid to do anything stupid on it. Take deep breaths. Don&#8217;t worry if you brick your phone, you can always unbrick it.

## <span id="Step_2_Backup_all_your_data">Step 2: Backup all your data</span>

Once you root your device, you&#8217;ll lose all the data stored your phone. So backup any sensitive data or media on a PC.

## <span id="Step_3_Root_your_Moto_G">Step 3: Root your Moto G</span>

Yes, root it. So what are the things you need for that.

  * A minimum of 70% battery charge on the phone (Not really necessary)
  * A USB cable
  * We assume that you have a PC

### <span id="Unlocking">Unlocking</span>

  * Configure your computer for fastboot.
  * Enable USB debugging on the device.
  * Connect the device to the computer through USB.
  * From a terminal on a computer, type the following to boot the device into fastboot mode

<pre>adb reboot bootloader</pre>

  * Once the device is in fastboot mode, verify your PC sees the device by typing

<pre>fastboot devices</pre>

> If you don&#8217;t see your device serial number, and instead see &#8220;**waiting for device**&#8220;, fastboot is not configured properly on your machine. See [fastboot](http://forum.xda-developers.com/showthread.php?t=2277112) documentation for more info.

If you see &#8220;**no permissions fastboot**&#8220;, try running fastboot as root.

  * From the same terminal, type the following command to obtain your bootloader unlock code:

<pre>fastboot oem get_unlock_data
</pre>

  1. Visit the [Motorola Bootloader Unlock](https://motorola-global-portal.custhelp.com/app/standalone/bootloader/unlock-your-device-a/action/auth) website and follow the instructions there to obtain your unlock key.
  2. If the device doesn&#8217;t automatically reboot, reboot it from the menu. It should now be unlocked.
  3. Since the device resets completely, you will need to re-enable USB debugging on the device to continue.

Ok it&#8217;s not done yet, that&#8217;s just rooting your device. You have to install a recovery.

### <span id="Placing_the_XposedFrameworkapk_in_the_phone">Placing the <a href="http://repo.xposed.info/module/de.robv.android.xposed.installer">XposedFramework.apk</a> in the phone.</span>

Download and move the [XposedFramework.apk](http://dl.xposed.info/modules/de.robv.android.xposed.installer_v33_36570c.apk) to your phone.

> This can be done later as well.

## <span id="Step_4_Recovery">Step 4: Recovery</span>

### <span id="Installing_Recovery_on_Moto_G">Installing Recovery on Moto G</span>

  1. Download recovery from [Unstable Apps Recovery Downloader](http://builder.unstableapps.com/#/latest/clockworkmodrecovery/falcon) to obtain the latest version of ClockworkMod recovery for your device.
  2. Connect the Moto G to the computer via USB.
  3. Make sure the fastboot binary is in your PATH or that you place the recovery image in the same directory as fastboot.
  4. Open a terminal on your PC and reboot the device into fastboot mode by typing by adb reboot bootloader using the hardware key combination for your device while it is powered off.
    
  5. Once the device is in fastboot mode, verify your PC sees the device by typing ``fastboot devices``
            
> If you don&#8217;t see your device serial number, and instead see &#8220;waiting for device&#8221;, fastboot is not configured properly on your machine. See fastboot documentation for more info.
  
> If you see &#8220;no permissions fastboot&#8221;, make sure your [UDEV](http://developer.android.com/tools/device.html) rules are setup correctly.
    
  6. Flash recovery onto your device by entering the following command: ``fastboot flash recovery your_recovery_image.img``
    where the latter part is the filename of the recovery image.
        
 7.Once the flash completes successfully, reboot the device into recovery to verify the installation. Boot to recovery instructions: Hold **Volume Down** & **Power** simultaneously. On the next screen use **Volume Down** to scroll to recovery and then use **Volume Up** to select.
        
Recovery mode looks like this.
  
[moto g recovery mode](/images/recovery.jpg)
        
Reboot the device. Install [supersu](https://play.google.com/store/apps/details?id=eu.chainfire.supersu&hl=en) and [busybox](https://play.google.com/store/apps/details?id=stericson.busybox&hl=en).
        
> We are almost there&#8230;
        
## <span id="Step_5_Xposed_Framework">Step 5: Xposed Framework</span>
        
Now that you are done rooting your phone you can install [XposedFramework.apk](http://dl.xposed.info/modules/de.robv.android.xposed.installer_v33_36570c.apk) like any other android application.
  
Now it&#8217;ll ask for a reboot.
        
> If your Xposed Framework doesn&#8217;t work then you may have to install [supersu](https://play.google.com/store/apps/details?id=eu.chainfire.supersu&hl=en) and [busybox](https://play.google.com/store/apps/details?id=stericson.busybox&hl=en) on your device.
        
Xposed Framework will look like the below screenshot.
  
[moto g xposed framework screenshot](/images/xposed.jpg)
        
> You may have to reboot a lot many times than usual, but it&#8217;s worth it.
        
## <span id="Step_6_GravityBox">Step 6: GravityBox</span>
        
Now in **Xposed Framework** navigate to **Download** click on search icon, type **GravityBox** and install it.
        
> That&#8217;s all, you are good to try all the customizations now.
        
# <span id="What_I8217ve_done_with_my_mobile">What I&#8217;ve done with my mobile.</span>
        
I have installed some modules like
        
  1. GravityBox (great way to customize your phone)
  2. Greenify (saves a lot of battery juice)
  3. MiniGuard (no ads in selected apps!)
  4. Tinted Status Bar (status bar takes up the color of the app you have launched)
  5. Xtended NavBar (navigation bar can be swiped to have music control buttons and quick toggles)
  6. XuiMod (some animation and stuff)

Read: <a href="http://redgadgets.com/save-battery-android-smartphone/" target="_blank">How to save battery on android smartphone?</a>

## <span id="How_does_it_looks_like">How does it looks like?</span>

> Here I have changed my status bar color. Usually the icons will be white, I have changed them to cyan. The tiles on the second screenshot are not available in stock ROM. I have quick toggle tiles that are really awesome. There is a camera tile, on clicking which you can take photos rightaway. No need to open camera app! The navigation bar is already using the **Android L** navbar. This is cool right?

[custom status bar Moto G](/images/statusbar.jpg)

> **Xtended NavBar** does some cool stuff with your navigation bar. You can now swipe it and control music and other toggles. Not a great deal but once you get used to this then you&#8217;ll know how hard it is to pull down and click on a quick toggle to turn your Wi-Fi on!

![Custom navbar Moto G](/images/navbar.jpg)

> Finally the **GravityBox**. This is the module through which you can change almost anything on your phone. By far this is the best module I have found. All those quick toggles you saw on the first screenshot was because of GravityBox. Customize your phone as you like. There are youtube videos available on how to use GravityBox!

![Gravity box for Moto G](/images/gravitybox.png)

Do you think Xposed Framework is better than a Custom Rom? Let us know in the comment section.

Thanks!