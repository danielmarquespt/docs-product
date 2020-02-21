---
summary: >-
  Learn how to quickly test your mobile app on a device, as soon as you publish
  and without the need of a developer account on Android or iOS.
tags: runtime-mobile
---

# Test Your Mobile App in the Device Using OutSystems Now

While developing your mobile app, you will need to run it to check the app functionalities and look and feel. In Service Studio you can do it by clicking on the "Test in Browser" option. However, you are limited since you can't test the mobile native capabilities of the device being called by your application, as the camera or the accelerometer.

To test a mobile app on your device and get the real behavior of the app, you usually have to [generate the application package](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/deliver-mobile/generate-and-distribute-your-mobile-app/intro.md%3E) for the target mobile operating system and install it on your device.

Using the [OutSystems Now app](https://now.outsystems.com>), you can test it on a device without having to generate the native application package and install it. You are able to execute and preview the plugins supported by OutSystems of your mobile device and debug your app, this way performing most useful tests, more often and get most accurate test results when compared to run it in the browser. OutSystems Now is a mobile app that loads your app in a container and provides a seamless integration between your app and the mobile functionalities.

To test a mobile app on your device using OutSystems Now:

1. Install the OutSystems Now app on your mobile device \(available for iOS and Android\). Skip this step if you have it already installed. 
2. Open the application that you want to test in Service Studio. 
3. In the application overview, open the Native Platforms tab. There you will find a Test option and a QR Code that will allow you to test your app using OutSystems Now. 
4. Open OutSystems Now app and scan the QR Code. 

While developing and publishing the app, the changes are automatically synced without the need of having to reopen the app.You can also check the [supported plugins provided by OutSystems Now](../extensibility-and-integration/mobile-plugins/intro.md#Supported_Plugins%3E).

