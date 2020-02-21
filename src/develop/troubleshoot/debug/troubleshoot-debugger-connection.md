---
summary: >-
  Troubleshoot issues that can arise while connecting your mobile device to your
  PC for debugging purposes.
tags: runtime-mobile; support-application_development; support-Mobile_Apps
---

# Troubleshoot Debugger Connection Issues

 Use Service Studio 11.5.44.2557 or later to debug the mobile apps if you generate them with MABS 6.

When trying to debug a mobile application using Google Chrome or a real device some issues can arise, like a firewall blocking local ports or a device not being discovered by Service Studio.

Below you can find a list of the most common problems that you may find when you are starting a mobile app debug session, as well as suggestions for fixing them.

## Issues Related With Unavailable Local Ports

The mobile app debugger feature of Service Studio requires one or two available local ports according to the debugging target:

When debugging on an Android device or in Google Chrome : One available port in the development machine starting at port 9222. If this port is unavailable, port 9223 will be checked and so on.

When debugging on an iOS device : Two available local ports in the development machine starting at port 9221. If this port is unavailable, port 9222 will be checked and so on.

If no available ports are found because they are in use or they are blocked \(e.g. by a firewall\), you will not be able to debug your mobile app in Service Studio.

## Issues While Connecting an Android Device

Check the following sections for more information on how to solve these issues:

* [USB/Android Debugging not enabled in device](troubleshoot-debugger-connection.md#usbandroid-debugging-not-enabled-in-device%3E)
* [Device not recognized by Windows](troubleshoot-debugger-connection.md#device-not-recognized-by-windows%3E)
* [Incompatible USB mode selected in device](troubleshoot-debugger-connection.md#incompatible-usb-mode-selected-in-device%3E)
* [USB Debugging was not allowed in device](troubleshoot-debugger-connection.md#usb-debugging-was-not-allowed-in-device%3E)
* [More than one Android device is connected to your PC](troubleshoot-debugger-connection.md#more-than-one-android-device-is-connected-to-your-pc%3E)

### USB/Android Debugging not enabled in device { \#usbandroid-debugging-not-enabled-in-device }

For the device to be detected by Service Studio, you should start by having the USB debugging \(or Android Debugging\) option enabled.

1. Navigate to the **Developer options** section inside the **Settings** and enable the **USB debugging** option.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/troubleshoot/debug/images/device-usb-debugging.png%3E)

   _Note:_ If you don't have the **Developer options** section in **Settings**, check how to [enable **Developer options**](https://developer.android.com/studio/debug/dev-options.html#enable>) on your device.

### Device not recognized by Windows { \#device-not-recognized-by-windows }

After ensuring that the USB debugging option is enabled, you should check if the device is detected by Windows and its drivers are correctly installed:

1. Open **Control Panel**.
2. Navigate to the **Hardware and Sound** category.
3. Open **Device Manager**, located under **Devices and Printers**.
4. If your device is listed under **Other devices**, you need to install the correct drivers before proceeding:

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/troubleshoot/debug/images/device-unrecognized.png%3E)

To help Windows correctly detect the device, follow [this guide](https://developer.android.com/studio/run/oem-usb.html>) to install the drivers provided by the manufacturer.

If after following the guide mentioned above Windows still fails to recognize the device properly, try using the drivers provided by Google by taking these steps:

1. Download the [Google USB Driver ZIP file](https://developer.android.com/studio/run/win-usb.html>) and extract it \(to the Desktop, for example\).
2. Right-click on your device and select **Update Driver Software...**.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/troubleshoot/debug/images/device-update-driver.png%3E)

3. Choose **Browse my computer for driver software**.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/troubleshoot/debug/images/device-browse-for-driver.png%3E)

4. Choose **Let me pick from a list of device drivers on my computer**.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/troubleshoot/debug/images/device-pick-driver-from-list.png%3E)

5. Select **Show All Devices** and click **Next**.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/troubleshoot/debug/images/device-show-all-devices.png%3E)

6. Choose the option **Have Disk...**, browse to the `usb_driver` folder located on the extracted folder and click **OK**.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/troubleshoot/debug/images/device-install-from-disk.png%3E)

7. Select **Android ADB Interface** and click **Next**.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/troubleshoot/debug/images/device-android-adb-interface.png%3E)

8. Confirm the installation of the driver by pressing **Yes**.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/troubleshoot/debug/images/device-driver-warning.png%3E)

9. Install the driver by choosing **Install**.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/troubleshoot/debug/images/device-driver-install-prompt.png%3E)

When the installation completes, press **Close** and check that the device appears in Device Manager:

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/troubleshoot/debug/images/device-install-success.png%3E)

### Incompatible USB mode selected in device { \#incompatible-usb-mode-selected-in-device }

The USB mode which the device is configured to use when connecting to a PC can also cause issues in the device detection process.

Depending on the version of Android and the manufacturer of the device, this option can be in different places. First of all, check if you have any notification referring to the USB mode, like the ones below:

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/troubleshoot/debug/images/device-usb-mode-1.png%3E)

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/troubleshoot/debug/images/device-usb-mode-2.png%3E)

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/troubleshoot/debug/images/device-usb-mode-3.png%3E)

If you find these options, try to switch between them \(`MTP`, `PTP` and `Camera` modes\), disconnecting and reconnecting the device to the PC and retrying the device discovery in Service Studio.

### USB Debugging was not allowed in device { \#usb-debugging-was-not-allowed-in-device }

Whenever an Android device is connected to a PC, a request to allow USB Debugging is shown on the device. This request should be accepted so that Service Studio can communicate with the device.

If you get a pop-up on your device like the one below, just tap **OK** and try again on Service Studio to detect the device:

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/troubleshoot/debug/images/device-allow-usb-debugging.png%3E)

### More than one Android device is connected to your PC { \#more-than-one-android-device-is-connected-to-your-pc }

Only one device from each platform \(Android/iOS\) can be connected to the PC for the device discovery process to run successfully.

Ensure that you only have one Android device connected to your PC.

## Issues While Connecting an iOS Device

Check the following sections for more information on how to solve these issues:

* [iTunes is not installed on your PC](troubleshoot-debugger-connection.md#itunes-is-not-installed-on-your-pc%3E)
* [Web Inspector is not enabled on your device](troubleshoot-debugger-connection.md#web-inspector-is-not-enabled-on-your-device%3E)
* [PC is not trusted for debugging](troubleshoot-debugger-connection.md#pc-is-not-trusted-for-debugging%3E)
* [More than one iOS device is connected to your PC](troubleshoot-debugger-connection.md#more-than-one-ios-device-is-connected-to-your-pc%3E)

### iTunes is not installed on your PC { \#itunes-is-not-installed-on-your-pc }

One of the requirements for the debugger to work with iOS devices is the iTunes installation on the machine where Service Studio is executing. Please make sure that you have it installed on your machine before trying to perform any debug session with an iOS device.

[Download the latest version](https://www.apple.com/itunes/download/>) from Apple's website.

_Note:_ If you installed iTunes from the Microsoft Store you must have iTunes running to be able to debug OutSystems mobile apps in iOS devices.

### Web Inspector is not enabled on your device { \#web-inspector-is-not-enabled-on-your-device }

 For checking network requests in iOS apps built with MABS 6.0 and later, use the \[build-in network inspection tool\]\(../inspect-http-requests-mobile.md\).

To ensure that your device is correctly detected you should make sure that the Web Inspector is enabled.

Do the following:

1. On your iOS mobile device tap Settings &gt; Safari &gt; Advanced.
2. Make sure that the "Web Inspector" option is turned **on**.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/troubleshoot/debug/images/ios-web-inspector.png%3E)

### PC is not trusted for debugging { \#pc-is-not-trusted-for-debugging }

The final step to setup your device to be ready for debugging is to trust the PC so it can communicate with the device. To do so, tap **Trust** when the following pop-up appears on your device:

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/troubleshoot/debug/images/device-trust-computer.png%3E)

Check [Apple Support](https://support.apple.com/en-us/HT202778>) for more information on trusted computers.

### More than one iOS device is connected to your PC { \#more-than-one-ios-device-is-connected-to-your-pc }

Only one device from each platform \(Android/iOS\) can be connected to the PC for the device discovery process to run successfully.

Ensure that you only have one iOS device connected to your PC.

## Issues During App Detection by Service Studio

When starting a new debug session using a device, and after the device has been correctly detected, Service Studio will start to actively look for the mobile app that you are debugging.

If you find issues during the app detection step \(e.g. the detection is taking too long\), make sure that the mobile app was generated with the `Debug` Build Type for Android and `Development` Build Type for iOS.

If your app is still not detected, try performing each of the following steps in your device and check if any of them solves your problem:

* Close all other running OutSystems mobile apps.
* Close the "OutSystems Now" mobile app.
* Close any browser app that could be running.
* Close all running apps.

