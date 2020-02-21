---
summary: >-
  More information on the data presented in the "Native Platforms" tab of
  Service Center.
tags: runtime-mobile
---

# Native Platforms Configuration

The Native Platforms tab in Service Center presents the following information:

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/deliver-mobile/generate-and-distribute-your-mobile-app/images/sc-native-platforms-table.png%3E)

Platform : The mobile platform being configured: iOS or Android.

Package of Last Tagged Version  
: Details of the latest package built from the last tagged version. Contains information on the version number, version code and MABS version used to generate the mobile app package.

```text
There are two operations available in this column:  

— **Download App Package**: Allows you to download the APK/IPA file of the displayed package, according to the current mobile platform.  

— **Download Mobile App Build Logs**: Allows you to download the build logs of the displayed package for the current platform. For more information check [Download Mobile App Build Logs](<intro.md#download-mobile-app-build-logs>).

**Note:** You will only have information in this column (and the operations described above) will  only be available if the version number of the latest mobile app package **matches the version number being displayed** for the current mobile platform in the Version > "Number" column.  
E.g. if you did changes to the app or to its configuration, the version number will (in most cases) contain a "+" stating that the last tagged version was changed. Since there is no mobile package available for this changed version, the "Package of Last Tagged Version" column will be empty.
```

Version  
: Version information and package status for the current mobile platform. Contains the following sub-columns:

```text
— **Status:** Shows any messages or warnings related to the mobile package for the current mobile platform. These messages are also shown in the application detail screen.  
For example, it can contain:  
a) A blue "**i**" icon with a message stating that the mobile platform is not configured yet.  
b) A yellow "**!**" icon with a warning stating that you need to generate your mobile app package. 

— **Number:** Contains the version number from the last tag operation done in LifeTime. 

— **Code:** An automatically incremented number, unless configured manually. For more information check [Customizing the Mobile App Version Code](<intro.md#customizing-the-mobile-app-version-code>).
```

Settings : Allows you to configure the settings for the current mobile platform. For more information check [Configure and Generate a Mobile App Package in Service Center](intro.md#configure-and-generate-a-mobile-app-package-in-service-center%3E).

Domain Name : Current domain name for the mobile app \(this setting is common to all mobile platforms\). For more information check [Customizing the Mobile App Domain Name](intro.md#customizing-the-mobile-app-domain-name%3E).

