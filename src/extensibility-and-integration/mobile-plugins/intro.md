---
summary: Extend the functionalities of your mobile apps by using plugins.
tags: >-
  runtime-mobile; support-application_development; support-Mobile_Apps;
  support-Mobile_Apps-featured
---

# Mobile Plugins

When developing a mobile app you often want to use the capabilities of the mobile device, such as the GPS or notifications. You can achieve this in OutSystems using plugins. A plugin is a module that acts as a wrapper for an Apache Cordova plugin and enables you to use native mobile features.

You can find [ready-to-use plugins in Forge](https://www.outsystems.com/forge/#category=plug-ins>), which contains both officially supported plugins and plugins created by the OutSystems Community. If you want to create your own plugins for use in mobile apps, do it by [wrapping an Apache Cordova plugin into a module](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/extensibility-and-integration/mobile-plugins/using-cordova-plugins.md%3E).

## Using a Mobile Plugin

[Install the plugin](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/getting-started/component.md%3E) in the environment as any other component. Use the client actions of the plugin module to call the native capabilities of the device within your application. The plugin must support the mobile platforms \(iOS, Android\) for which you are creating an app or the app generation will fail.

Each time you add, remove, or modify the plugin in an app, OutSystems [rebuilds the native shell](../../deliver-mobile/mobile-app-update-scenarios.md#Situations_When_the_User_Must_Install_a_New_Build%3E) which you then have to distribute to the end-users for installation.

You must [include the plugin license](../../deliver-mobile/compliance-with-third-party-licenses.md#Include_the_Third_Party_Licenses_Used_by_Plug-ins_or_Components%3E) in your app to respect the license agreements of that plugin. Usually, these license agreements are placed in the About page of the app that uses them.

## What Are the Supported Plugins Provided by OutSystems { \#Supported\_Plugins }

This is the list of officially supported mobile plugins. Most of these plugins are included in the [OutSystems Now app](https://now.outsystems.com/>) for an out-of-the-box testing.

| Plugin | Description |
| :--- | :--- |
| [Camera](http://www.outsystems.com/forge/component-discussions/1390/Camera+Plugin>) | Enable your application to access the camera capabilities of the device. |
| [Ciphered Local Storage](https://www.outsystems.com/forge/component-details/1500/ciphered-local-storage-plugin/>) \(not included in OutSystems Now\) | Keep your mobile application's sensitive data safe using a ciphered Local Storage database. |
| [Card IO](https://www.outsystems.com/forge/component/1438/card-io-plugin/>) | Automatically get the details of a credit card just by taking a picture. |
| [OneSignal Notifications](http://www.outsystems.com/forge/component/2119/onesignal-plugin/>) \(not included in OutSystems Now\) | Push Notifications using OneSignal, with deep-linking and actions. |
| [Pushwoosh Notifications](http://www.outsystems.com/forge/component/1556/pushwoosh-plugin/>) \(not included in OutSystems Now\) | Push Notifications using Pushwoosh, with deep-linking and actions. |
| [SSL Pinning](https://www.outsystems.com/forge/component-discussions/1873/SSL+Pinning+Plugin>) \(not included in OutSystems Now\) | Provide an extra layer of security to HTTPS communications by adding a verification of the server certificate against hashes of public keys. |
| [Local Notifications](http://www.outsystems.com/forge/component/1541/local-notifications-plugin/>) | Send app notifications to the device when the application isn't running in the foreground. |
| [QR/Barcode scanner](https://www.outsystems.com/forge/component/1403/barcode-plugin/>) | Scan barcodes and QR codes. |
| [Location](https://www.outsystems.com/forge/component/1395/location-plugin/>) | Access the GPS capabilities of the user's device. For example the latitude, longitude and the altitude of the user's device. |
| [Contacts](http://www.outsystems.com/forge/component-discussions/1394/Contacts+Plugin>) | Access the contacts of your device. |
| [InApp Browser](https://www.outsystems.com/forge/component/1558/inappbrowser-plugin/>) | Open external URLs directly in your application. |
| [Touch ID](https://www.outsystems.com/forge/component-details/1431/Touch+ID+Plugin/>) | Use authentication with Touch ID in your application. |
| [Calendar](https://www.outsystems.com/forge/component/1566/calendar-plugin/>) | Access the calendar of your device. |
| [Key Store](https://www.outsystems.com/forge/component/1550/Key+Store+Plugin/>) | Store small amounts of sensitive information on your device. The keystore secures data by encrypting the data before storing it, and the platform itself carefully controls access to stored items. |

## Built-in Plugins

Mobile apps generated by OutSystems have a native shell with the following plugins which OutSystems uses internally. You may see the names of these plugins in the [native mobile shell logs](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/monitor-and-troubleshoot/monitoring-an-environment.md%3E).

| Plugin | Description |
| :--- | :--- |
| OS Cordova Loader | Loads the Cordova engine on your app. |
| OS Security | Provides the required APIs for the security layer. |
| OS Manifest | Provides a parser for the app manifest. |
| OS Pre-Bundle | Handles the content of pre-bundled resources on your app. |
| OS Cache | Allows your application to run offline or with bad network conditions. |
| OS Deeplinks | Allows opening hyperlinks to specific screens of your app. |
| OS DB Upgrader | Manages the local storage of your app. |
| NetworkStatus | Allows your application to know when the device is online, offline and the type of network available \(Wifi, 3G, 4G...\). |
| Mobile AppFeedback | Enables the user to invoke App Feedback for submitting feedback about the app. \(Only present in the native shell if the App Feedback feature is [enabled](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/managing-the-applications-lifecycle/app-feedback/user-feedback-enable.md%3E) in the mobile app.\) |

