# SDK Changes (v4 and lower)

<!-- tabs:start -->

#### ** SDK (v4 and Lower) **

###  Version 4.2.1 *(12-04-2021)*

**New Features**
 * _Lotame Module_: Added new module that incorporates the Lotame SDK used for tracking IAP and advertisement analytics.

**Bug fixes**
 * Android/iOS: Fixed several issues regarding advertising.
 * Unity Editor: Fixed displaying issue with dummy banner placements.

**Other**
 * Android: Added support for Billing Library v3. Both old AIDL implementation as well as the new Billing Library will be supported by the SDK.
 * Android/iOS/Unity/Cordova: Added support for first time offline usage for the Localization feature. When building the game, make sure that the 'defaultLocalizationData.json' file is present in your assets in order for this to work. The local file will always contain the default language.
 * Android/iOS/Unity: Added support of custom callbacks per PlayerData operations for Wallet and Inventory (Add, Subtract, Open Gacha, Buy Bundle). For more information check the the Wallet and Inventory documentation.
 * Android/iOS: Updated AdMob to latest version and all ad mediation networks.
 * Android/iOS: Updated to the latest AppsFlyer SDK.
 * Android: Migrated the SDK from Bintray to MavenCentral.

###  Version 4.1.0 *(28-01-2021)*

**New Features**
 * _Localization_: This feature provides localization for your games. In order to configure localizations for your games please consult the documentation for both the Console and the SDK.

**Bug fixes**
 * Android: Fixed issue with incorrect tracking of session stops and heartbeats when ads and splash screens are shown.
 * Android: Fixed several minor crashes.
 * Unity Editor iOS: Fixed issue with the Privacy Policy not initializing the SDK.
 * Unity: Refactored and fixed the WebGL platform support.

**Other**
 * Android/iOS/Unity/Cordova: Implemented logic to filter out events using the Gamedock backend.
 * Android/iOS/Unity/Cordova: Implemented logic to disable event sending (archiving a game).
 * Android/iOS/Unity: Added method to show the app settings screen.
 * Android/iOS/Unity/Cordova: Removed Adjust module.
 * Unity: Removed AAR support for the Android dependency management.
 * Unity: Added new functionality to easily import or update the Android dependencies via Gradle, using only the Unity supplied gradle (or your own custom one).
 * iOS: Added functionality to request ATTracking permission without using the Privacy Policy.
 * iOS: Added functionality for Rich Push Notifications.

###  Version 4.0.2 *(02-12-2020)*

**Bug fixes**
 * Android: Fixed issue with IAP packages not being initialized/returned correctly.

###  Version 4.0.1 *(23-11-2020)*

**Bug fixes**
 * Android: Fixed crash related to ad tracking.
 * Android: Fixed crash related to decrypting event values.
 * Android: Added potential fix for saving information to shared preferences async.

**Other**
 * Android: Updated AdMob to latest version and all ad mediation networks.
 * iOS: Added more SKAdNetwork ids for several mediation networks.

###  Version 4.0.0 *(07-11-2020)*

**New Features**
 * _Gamedock Ads Module_: This feature enabled internal ads (from within Azerion) to be displayed within the Gamedock SDK using the Priority Ads feature.
 * _iOS 14 Support_: The SDK was updated to support iOS 14 including the new permission requirement from Apple regarding Ad Tracking. The GDPR popup for iOS now has an extra permission pop up after the user has accepted it. This permission cannot be customized and needs to come directly from Apple.
 * _Ogury Mediation Network_: A new ad network was added to the AdMob mediation stack.

**Bug fixes**
 * Android/iOS: Fixed issue with sending correctly the AppsFlyer id to the Gamedock Backend.
 * iOS: Fixed issue with Age Gate not taking into account properly the settings.
 * iOS: Fixed issue with push notifications tokens not being parsed correctly. 
 * Android: Fixed issue with doing an "AddItem" operation with the Transaction Builder.
 * Android: Fixed issue with AppsFlyer id not being sent with the SDK "install" event.
 * Android: Fixed several minor ANR and Crashes.

**Other**
 * Android/iOS/Unity/Cordova: Updated GDPR flow to now by default have personalized content and ads be disabled by default. Changed the button from "Accept" to "Accept All" and updated the flow for saving the user's options to take into account the change.
 * Android/iOS: Updated AdMob mediation adapters and networks.
 * Android/iOS/Unity: Opening a gacha will now return the position of the received gacha content in the PlayerDataUpdated callback.
 * Android/iOS/Unity: Added additional claim method for tiered events.
 * Android/iOS: Added additional tracking for ad events (available/not available).
 * Android/iOS/Unity/Cordova: Retrieving the game config will no longer also return the SDK config.
 * Unity: When building the game, the SDK will automatically fetch the latest Default Configuration Files.
 * Unity: Renamed GachaContent, BundleItem and PackageItem to GachaEntity, BundleEntity and PackageEntity.

###  Version 3.9.1 *(04-06-2020)*

**Bug fixes**
 * Android: Fixed issue with custom set package names.
 * Android: Fixed critical issue with specific service crashing (reported in the Play Store console).
 * iOS: Updated all ad networks to have the UIWebView references warning be removed when uploading builds with Gamedock to the Apple Store

**Other**
 * Android/iOS: Updated AdMob mediation adapters and networks in order to fix crashes and have the improvements from those updates.


###  Version 3.9.0 *(26-05-2020)*

**New Features**
 * _Advertisement Initialization_: The SDK now reports back to the game when the advertisement module has been initialized. **Make sure to start using the ads methods after the "OnAdsInitialized" callback has been fired otherwise ads will not work properly! Check the documentation page for Advertisement for more information.** Additionally, the SDK now reports tracks internally the time it took to initialize each ad mediation partner.
 * _Multi-operation Wallet and Inventory Transactions_: It is now possible to perform multiple operations on the Wallet and Inventory, before committing and sending to the backend the information. All the operation will be grouped into one event thus allowing for easier tracking. The following operations are supported: *AddCurrency, SubtractCurrency, AddItem, SubtractItem, OpenGacha, AddUniqueItem, RemoveUniqueItem, UpdateUniqueItem*. For more information on how to use this, check the following page: [https://azerion.github.io/gamedock-sdk/#/shopWalletInventoryControl](https://azerion.github.io/gamedock-sdk/#/shopWalletInventoryControl).
 * _App Rate Screen_: This feature allows the displaying of a popup in which the user is asked to rate the game. If the user gives a rating lower than 4, the user is redirected to a provided feedback url. For more information, check the documentation here: [https://azerion.github.io/gamedock-sdk/#/appRate](https://azerion.github.io/gamedock-sdk/#/appRate).

**Bug fixes**
 * Android: Fixed crash related to IAP initialization.
 * Android: Fixed issue with AppsFlyer not tracking properly.
 * iOS: Fixed ad tracking for banner ads.
 * iOS: Renamed HookBridge method "cStringCopy" to "gdStringCopy" to avoid conflicts with other libraries.
 * Android/iOS: Excluded SDK reserved events from being tracked by Firebase.
 * Unity: Fixed issues with iOS post-build script.
 * Unity: Fixed issue with Editor inventory subtraction delta.
 * Unity: Fixed minor issue with Features Initialization when using social login in the editor.

**Other**
 * Android: Removed the Gamedock Firebase module. In order to use Firebase and the features supported by Gamedock make sure to include the dependencies mentioned at the bottom of this page: [https://azerion.github.io/gamedock-sdk/#/addingTheGamedockSDK](https://azerion.github.io/gamedock-sdk/#/addingTheGamedockSDK).
 * Android/iOS: Refactored AdMob implementation to use the new provided API which should improve loading times of ads. This ties in with the Advertisement Initialization feature. **Because of the new api, it is not possible anymore to track clicks on any rewarded video ads from AdMob or it's partners (the "rewardedVideoDidClick" event).**
 * Android/iOS/Unity: Refactored the way certain callbacks communicate between Unity and the native layer. The forward facing api will not change, but it does mean fewer native calls made from Unity towards the native layer (since the data is available in the initial callback). This can show slight improvements in performance and data reliability.
 * Android/iOS/Unity: Added minor feature to check which version id is received for specific configuration. Currently only Game Config is supported but more will be added later.
 * Android/iOS/Unity/Cordova: Added additional security to the SDK.
 * Android/iOS/Unity/Cordova: Added IAP subscription validation. If a subscription is valid it will be returned from the backend in the same callback as regular subscriptions. Make sure to mark the IAP purchase event that it is a subscription for this to work.
 * Unity: Changed default iOS module inclusion. The additional Gamedock iOS SDK modules are now disabled by default.
 * Unity: Added several helper methods for *PlayerDataHelper* and *GameDataHelper*.
 * Unity: All helpers (PlayerData, GameData, etc.) have been moved under *Gamedock.Instance*.
 * Android/iOS/Unity/Cordova: Added AdStart callback for when a banner is shown as well as notify which type of ad is shown through the AdStart callback
 * Android/iOS/Unity/Cordova: Updated Firebase and AppsFlyer libraries to the latest versions.
 * Android/iOS/Unity/Cordova: Updated Ad libraries to the latest versions.
 * Android/iOS/Unity/Cordova: Added minor additional tracking properties for advertisement requested events.


###  Version 3.8.1 *(25-02-2020)*

**Bug fixes**
 * Android: Fixed crash when the SDK thread is not created properly.
 * Android: Fixed crash where in certain cases the install store name could not be retrieved.
 * Android: Fixed ANR issue with the InitializationCompleted callback for Unity.
 * Android: Fixed few other ANR related issues.
 * iOS: Fixed issue when showing/hiding banner ads.
 * Unity: Updated Android post-build script to support Unity 2019.3.+ .
 * Unity: Updated iOS post-build script to support Unity 2019.3.+ .


###  Version 3.8.0 *(04-02-2020)*

**New Features**
 * _Priority Ads_: The SDK now allows the configuration of Priority Ads thorough the Gamedock Console. This feature allows adding ad placements (banners, interstitial and rewarded videos) as priority using different ad providers than the default stack. For example, Ad Manager ad unit ids can be shown X amount of times before the SDK then falls back to the default AdMob mediation stack. On the SDK side, no additional implementation is required as all configuration is done through the Console.
 * _Toggleable Features_: Most of the SDK features can now be turn on or off individually, thus potentially reducing the number of events fired automatically by the SDK. The SDK will report in it's logs if a feature is not enabled. Enabling/Disabling features is done through the Gamedock Console. In the Unity Editor, you can see the features overview in the Configuration->General tab.

**Bug fixes**
 * Android: Fixed issue with Unity Ads not displaying ads properly.
 * Android: Fixed several issues related to ad request/displaying.
 * Android: Fixed crash when displaying Splahscreens through WebViews.
 * Android: Fixed crash related to SDK threading.
 * Android: Fixed issue with displaying Unity Ads ads.
 * iOS: Fixed issue related to MissionData handling.
 * iOS: Fixed issue with Age Gate callback not forwarding the correct response for native implementations.
 * Cordova: Fixed initialization issue with IAP tracking.
 * Unity: Improved logging.
 * Unity: Fixed several warning messages.

**Other**
 * Android/iOS/Unity/Cordova: Direct interstitial requests will now take into account interstitial timers set in the Gamedock Console.
 * Android/iOS/Unity/Cordova: Added extra tracking for all advertisement placements (banners, interstitials, rewarded videos).
 * Android/iOS/Unity/Cordova: Added extra InitializationCompleted callback from the SDK when the initial initialization is completed (you should still listen to the various callbacks for each feature for more accurate functionality).
 * Android/iOS/Unity/Cordova: Updated Firebase libraries to the latest versions.
 * Android/iOS/Unity/Cordova: Updated Ad libraries to the latest versions.


### Version 3.7.0 *(20-11-2019)*

**IMPORTANT! If you are experiencing issues with missing scripts on some of our Editor prefabs, it is caused by Unity not importing properly some of it's components. In order to fix it please download [this](https://splashscreens.cdn.spilcloud.com/files/1574351079_Prefabs.zip) package and overwrite the folder "Assets/Gamedock/Editor/Prefabs".**

**New Features**
 * _Fyber Mediation and Awesome Ads_: Two new mediation networks have been added to the AdMob stack.
 * _Chartboost Refactoring_: The Chartboost module has been removed and Chartboost has been moved as a mediation inside AdMob.

**Bug fixes**
 * Unity: Fixed issue with FPS tracking creating an infinite value list.
 * Unity: Fixed issue with SDK Windows throwing exceptions when appearing in the editor.

**Other**
 * Android/iOS: Added new initialization flow (builder) for native initialization which can be used for native implementations of the SDK or for new engine plugins.
 * Android/iOS/Unity: Added new method to directly request an interstitial. The flow matches the requesting of rewarded videos.
 * Android/iOS/Unity: Added new method to directly check if an ad is available (banner, interstitial, rewarded video).
 * Android/iOS/Unity: Added new method to retrieve the Firebase Instance Id.
 * Android/iOS: Added additional mediation information to be sent with the SDK event when an interstitial is displayed (similar to rewarded videos).
 * Android/iOS/Unity: Added two new methods for passing GDPR (Privacy Policy) information and retrieving it.
 * Unity: Reduced size of the example assets for Privacy Policy and Age Gate.
 * Unity: Moved the JSONObject class to the Gamedock namespace.
 * Unity: Removed the Android Project Id value as that is not used anymore.
 * Android/iOS: Updated AdMob mediation networks.
 * Android/iOS: Added CCPA AdMob compliancy.


### Version 3.6.1 *(24-10-2019)*

**Bug fixes**
 * Android: Fixed issue with reward video initialization causing ANRs.
 * Android: Removed pre-caching of reward videos.
 * iOS: Fixed issue with native Age Gate and GDPR popups not displaying properly on iOS 13 and Night Mode.
 * iOS: Fixed issue with Age Gate not returning the correct age group in the callback.
 * Unity: Fixed several issues when requesting default configuration files

**Other**
 * Android: Updated Unity Ads SDK to 3.3.0.


### Version 3.6.0 *(08-10-2019)*

**IMPORTANT! The SDK has been migrated from Spil to the new Gamedock brand. This means that all API calls and references have been changed to Gamedock. Make sure to update all your references in order to get the SDK working again.**

**New Features**
 * _Migration to Gamedock_: The SDK has been rebranded to Gamedock meaning that all Spil/Spilgames references have been removed (as much as possible). Make sure to update your API calls/Gameobjects/Prefabs accordingly.
 * _AppsFlyer Module_: The AppsFlyer SDK has been added as a module. The module can be enabled/disabled in the Configuration screen under each platform.
 * _External Partner Ids_: The SDK now accepts the passing of external partner ids, either when initializing or at a later stage, in order to better connect tracking between the different SDK that you might be using (AppsFlyer, Steam, Facebook, etc.).

**Bug fixes**
 * Android: Fixed several ad related crashes and ANR issues.
 * Android: Fixed isolated cases where the SDK will fail to initialize properly.
 * Android: Fixed issue with GCM key retrieval causing ANRs; it has been replaced with FCM and now requires the Firebase module.
 * iOS: Fixed crash that could happen if certain Ad networks were enabled.
 * iOS: Fixed crash for WebView javascript data injection on iOS 13.
 * Unity: Fixed build errors caused by switching to WebGL/Standalone.
 * Unity: Fixed gradle script to include symbol uploading to Crashlytics.

**Other**
 * Android/iOS: Updated all Ad networks.
 * Android/iOS: Added myTarget mediation network.
 * Unity (experimental): Added Standalone support for SDK tracking and features (at the moment the following features are not supported: Splashscreens, Daily Bonus, Tiered Events, Ads).
 * Unity (experimental): Fixed WebGL support for the SDK tracking and features (at the moment the following features are not supported: Splashscreens, Daily Bonus, Tiered Events, Ads).
 * Unity: Added toggle to easily override the AppController for iOS.
 * Unity: Exposed the Android Crashlytics/Fabric api key to the manifest. If you are using a different Fabric account then the old Spilgames one, make sure to update this key.


<!-- tabs:end -->


