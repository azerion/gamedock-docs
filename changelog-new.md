# SDK Changes (v5 and higher)

> [!WARNING]
> Starting Unity SDK version 5.2.0; the SDK will be available via the Unity package manager, please read the [Upgrade Guide](upgradeUnitySDK.md)

<!-- tabs:start -->

#### ** Unity SDK **

## [5.3.8] - 02-12-2022
### Fixed
- WebRequest disposed to fix memory leaks when exporting
- Localization fixes
- GUID conflicts fixed

## [5.3.7] - 29-11-2022
### Fixed
- Android Sdk Azerion logo ratio fixed
- WebRequest disposed to fix memory leaks
- String.xml removed and checking removed

## [5.3.6] - 20-11-2022
### Fixed
- iOS Sdk Version upgraded

## [5.3.5] - 16-11-2022
### Fixed
- iOS Sdk Feature name fix

## [5.3.4] - 11-11-2022
### Fixed
- Android Sdk Minor version changes warning fixed
- Auto Translation Text Mesh Pro fixes

## [5.3.3] - 11-11-2022
### Fixed
- Android Sdk Dependency version fixed

## [5.3.2] - 10-11-2022
### Fixed
Gamedock Setting Android menu fixed

## [5.3.1] - 04-11-2022

### Added
getConsentStatus added for retrieving User Consent status added for Android

## [5.3.0] - 23-09-2022
### Changed
- Removed Gamedock Configuration from Editor menu and added new Settings to the menu.
- Removed GamedockSDK game object from the scene.
- All the Gamedock configurations/Settings are now managed via a single ScriptableObject named "GamedockSettings" (located inside Assets/Resources dir).
- Removed "Initialize On Awake" and "Dont Destroy On Load" option. 
- GamedockSDK gameobject is now created runtime when initialized from the script and set not to destroy on load.
- New "GamedockSettings" is platform specific, options are available based on current platform.
- "ATT Accepted" option is moved under Unity Editor Settings.
- Removed Ads, Daily Bonus, Token System settings
- Get User Consent Status
- [Android] Removed option to set "Custom Package Name".
- [Android] Removed defaultGameConfigAndroid, Now using only defaultGameConfig to store config data of all platform.
- [iOS] Removed option to set "Custom Bundle Id".
- [iOS] Removed GamedockSDKiOSConfig and moved necessary config options to new "GamedockSettings". 

## [5.2.4] - 13-10-2022
### Changed
- [Android] Target SDK was upgraded to 31
- [Android] Firebase dependencies were upgraded to latest versions
- [Android] play-services-basement dependency updated
- [Android] Latest Gamedock android sdk dependency updated


## [5.2.3] - 12-08-2022
## Changed
- [iOS] hotfix SDK implemented. Copying resource files function removed
- [Android] fixing  version problem fixed
- [Unity] creating user config assset bug fixed

## [5.2.2] - 25-07-2022
## Changed
- [iOS] SDK user data retrieving problem fixed
- [Android] post process duplicating some gradlea value problem fixed

## [5.2.1]
### Changed
- iOS SDK version problem fixed
- Android firebase frameworks upgraded

## [5.2.0]

### Changed
- Switched to UPM support, meaning you can now add the SDK via the Unity Package Manager
- ATT flow fixed. If user select 'Not Allow Tracking' privacy policy popup does not show
- Initialization bugs fixed.

### Removed
- Removed the option to 'use' Tracking files (C#) that could be fetched from a bucket

## [5.1.5] - 30-08-2022

### Added
- Android SDK Minor version changes warning removed
- in Configuration help android google billing dependency removed

## [5.1.4] - 21-06-2022

### Changed
- [iOS] Adjusted ATT Flow

## [5.1.3] - 01-06-2022

### Changed
- [iOS] Adjusted Header image in GDPR popup

## [5.1.2] - 16-05-2022

### Changed
- [iOS] Updated framework to resolve Firebase compile issues
- [Android] Updated SDK for Android 12 support

## [5.1.1] - 06-05-2022

### Added
- [Android / iOS / Unity] Added OnAdTrigger for interstitial trigger on gamedock event

### Changed
- [Unity / iOS] Updated firebase so it builds again for iOS

## [5.1.0] - 04-04-2022

### Added
- Added Support for Azerion Connect
- Added Device ID to ZendeskWebview

### Removed
- Removed Lotame SDK support


## [5.0.0] - 01-01-2022

### Changed
- Update .gitignore to match modern day
- Updated Changelog, [2.1.0] to [3.5.0] are documented in CHANGELOG.old, [3.5.0] to [4.2.1] can be found on github as combined log for all SDK targets
- [iOS] Adjusted flow for Apple ATT popup to comply with Apple's rules
- [Unity] Adjusted Privacy Policy Prefab to work in correct flow with new Apple ATT popup

### Removed
- [Android / iOS] AppsFlyer SDK has been removed, maintenance shifted towards game projects
- [Android / iOS] Ads and Admob SDK (including all Mediation adapters) have been removed, they are to be replaced with the new Azerion AD SDK in the game projects
- [Android] Removed all jcenter and bintray gradle references, because these have been [closed](https://developer.android.com/studio/build/jcenter-migration)
- [Unity] Removed newtonsoft dll file, can be installed via Unity package manager instead

### Fixed
- [Android / iOS] Text bug in GDPR / Privacy Policy screen
- [Android] Fixed an issue where the AndroidBuildPostProcessor would incorrectly overwrite the gradle properties


#### **Cordova SDK **

## [5.3.3] - 02-12-2022
### Changed
- Android SDK dependency version upgraded

## [5.3.2] - 20-11-2022
### Changed
- iOS SDK dependency version upgraded

## [5.3.1] - 04-11-2022

### Fixed
new android dependency added

## [5.3.0] - 04-11-2022

### Added
5.3.0 iOS And Android dependencies added
getConsentStatus function added

## [5.2.1] - 13-10-2022
### Changed
- [Android] Target SDK was upgraded to 31
- [Android] Firebase dependencies were upgraded to latest versions
- [Android] play-services-basement dependency updated
- [Android] Latest Gamedock android sdk dependency updated

## [5.2.0]
### Changed
- [Android / iOS] Upgraded the native Gamedock SDK's to [5.2.x] hotfix branches

## [5.1.0]
### Added
- AdTrigger Callback to show ad after gamedock event

### Changed
- [Android / iOS] Upgraded the native Gamedock SDK's to [5.1.x]


## [5.0.0] - 02-03-2022

### Added
- Added some button for other API calls like getting the user/device id and triggering a iapPurchased event

### Changed
- [Android / iOS] Upgraded the native Gamedock SDK's to [5.0.0]

### Removed
- Removed all the ad related content

#### **iOS Native SDK **

## [5.3.2] - 20-11-2022
### Fixed
- GetConsent bug fixed

## [5.3.1] - 15-11-2022
### Changed
- MoreApps feature name fixed

## [5.3.0] - 04-11-2022

## Changed
Encryption algorithm changed

## Removed
Tiered Events

## [5.2.7] - 30-09-2022

## Added
getConsentStatus added for retrieving User Consent status

## [5.2.5] - 12-08-2022

## Added
Resources files were path changed to pod directory. No need to copy resource files into main bundle

## [5.2.2] - 25-07-2022

## Changed

iOS User Data retrieving problem fixed


## [5.2.1]

### Changed

iOS SDK version problem fixed

## [5.1.1] - 06-05-2022
### Added
- Add OnAdTrigger event that will allow a game developer to show interstitials after a gamedock event

### Changed
- Updated Firebase so it works with iOS again
- Native Privacy Policy Popup opening conditions fixed


## [5.1.0] - 01-04-2022
### Added
- Added Support for Azerion Connect
- Added Device ID to ZendeskWebview

### Removed
- Removed Lotame SDK support


## [5.0.0] - 01-02-2022


### Changed
 - Update .gitignore to match modern day
 - Updated Changelog, [2.1.0] to [3.5.0] are documented in CHANGELOG.old, [3.5.0] to [4.2.1] can be found on github as combined log for all SDK targets
 - Adjusted flow for Apple ATT popup to comply with Apple's rules
 - 
### Removed
 -  AppsFlyer SDK has been removed, maintenance shifted towards game projects
 -  Ads and Admob SDK (including all Mediation adapters) have been removed, they are to be replaced with the new Azerion AD SDK in the game projects

### Fixed
 - Text bug in GDPR / Privacy Policy screen


#### ** Android Native SDK **

## [5.3.2] - 29-11-2022
### Changed
- azerion logo ratio changed on privavcypolicy and age gate pages

## [5.3.1] - 04-11-2022

### Added
getConsentStatus added for retrieving User Consent status


## [5.3.0] - 04-11-2022

### Changed
Encryption algorithm changed

### Removed
Tiered Events

## [5.2.3] - 22-09-2022

### Changed
google play-services dependencies were upgraded to latest versions

## [5.2.2] - 13-09-2022
### Changed
- Target SDK was upgraded to 31
- Firebase dependencies were upgraded to latest versions
- play-services-basement dependency added
- Target SDK upgraded encryption sdk integrated

## [5.2.1]
### Changed
- Version number was changed to equal with unity sdk hotfix version
- Firebase config sdk version increaded

## [5.2.0]
### Changed
- Age gate and privacy policy popups header image changed. Logo of Azerion is in middle
- Large heap allowed in manifest file. This is fixing the out of memory crash in older android devices
- Server Time parameter null check added to prevent possibility of crashes
- Updated Firebase packages to latest versions

### Added
- Exported true parameter added to support android 12
- Clear Text network traffic was disabled

## [5.1.3] - 13-05-2022
### Added
- Add OnAdTrigger event that will allow a game developer to show interstitials after a gamedock event
- Added exported:true to net.openid.appauth.RedirectUriReceiverActivity to comply with Android 12 / Target 31


## [5.1.0] - 01-04-2022

### Added
- Added Support for Azerion Connect
- Added Device ID to ZendeskWebview

### Removed
- Removed Lotame SDK support


## [5.0.0] - 01-02-2022

### Changed
 - Update .gitignore to match modern day
 - Updated Changelog, [2.1.0] to [3.5.0] are documented in CHANGELOG.old, [3.5.0] to [4.2.1] can be found on github as combined log for all SDK targets

### Removed
 - AppsFlyer SDK has been removed, maintenance shifted towards game projects
 - Ads and Admob SDK (including all Mediation adapters) have been removed, they are to be replaced with the new Azerion AD SDK in the game projects
 - Removed all jcenter and bintray gradle references, because these have been [closed](https://developer.android.com/studio/build/jcenter-migration)

### Fixed
 - Text bug in GDPR / Privacy Policy screen

<!-- tabs:end -->


