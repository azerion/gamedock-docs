# Change Log

<!-- tabs:start -->

#### ** Android SDK **

## [5.1.5] - 30-08-2022

### Added
- Android SDK Minor version changes warning removed
- in Configuration help android google billing dependency removed

#### ** Unity SDK **

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

#### ** Android Native SDK **

## [5.0.0] - ??-??-????

#### ** iOS Native SDK **

## [5.0.0] - ??-??-????

#### ** Cordova Plugin SDK **

## [5.0.0] - ??-??-????


#### ** Console **


### 01.03.2021 - 31.03.2021

* Added filtering on tags for localization texts.
* Added highlighting for template variables in localization texts.

### 01.02.2021 - 28.02.2021

* Added "create another" option in modals.
* Improve configuration for the Unknown Keys section of Localization.
* Add images to the keys description in Localization.
* Redesign the datatable Modals.

### 01.01.2021 - 31.01.2021

* Added game and sdk version overview for management and organisation page.
* Refactored the Notification pages.
* Improved certain UX/UI aspects of the Localization feature.
* Added release overview page and add release notes link.

### 01.12.2020 - 31.12.2020

* Changed AppsFlyer attribution versioning to an ignore list.
* Revamped data view modal, change jsonviewer to vue and add url renderer.
* Completed Localization feature.

### 01.11.2020 - 30.11.2020

* Added wildcard permissions. 
* Fixed visual bug in User roles page.
* Updated the Tiered Events pages to match latest visual standards.
* Added default versions and SDK config for new created games.
* Improved Virtual Goods navigation flow.
* Fixed several form related bugs.
* Added AppsFlyer whitelisted flag to tracked devices.
* Added game deletion for organisations.
* Added first parts of the Localization feature.

### 01.10.2020 - 31.10.2020

* Updated GDPR popup partner list.
* Added redirect for user to Store page when no stores present on IAP Validation page.
* Fixed test devices labelled wrongly as 'None' in Campaigns.
* Removed Chartboost configuration.
* Added custom types for push notifications.
* Improved User Permission feedback.
* Additional UX improvements.

### 01.09.2020 - 30.09.2020

* Added description to event game versions and properties.
* Added pushNotification statistics to the user page.
* Made 404 and 500 error pages prettier.
* Fixed Shop management page structure.
* Fixed Management menu item not stuck to bottom.
* Added possibility for user to manually configure IAP validation.
* Additional UX improvements.

### 01.08.2020 - 31.08.2020

* Removed Franchises field from the games.
* Removed DFP entries from the Advertisement page.
* Added testing functionality to push notifications.
* Added Event Dashboard overview and removed event validation page.
* Added 404s when the user doesn't have permission to view games and organisations.
* Added Game Viewer role to users that have custom roles.

###  01.07.2020 - 31.07.2020

* Push notifications improvements.
* Added button to see all Graphana graphs below graph.
* Added new Priority Ads network.
* Added new Help Texts connected to GitHub.
* Changed Event Dashboard devices to be game specific.

###  01.06.2020 - 30.06.2020

* Added validation before deleting a creative.
* Minor issue fixed with pop-ups.
* Push notifications improvements.
* Changed so that super users see all games for permissions.
* Permissions system improvements.
* Several UI/UX improvements.

###  01.05.2020 - 31.05.2020

* Added redirect for campaigns if the game is not correct.
* Bug fixes and improvements for Organizations and Role Management.
* Removed old permissions system (replaced by the Organization and Role Management features).
* Added confirmation window before removing a Splashscreen creative.

###  01.04.2020 - 30.04.2020

* Re-added campaigns for promotions.
* Added Audit logs for push notifications.
* Added Audit logs for event configurations.
* Fixed issue with date formatting for Audit Logs.
* Added the Organizations feature.
* Added the Role Management feature.
* Improved Advertisement statistics.
* Removed testing environment on several features.
* Added extra Firebase key for Android SDK Config.

###  01.03.2020 - 31.03.2020

* Added generic Audit logging page.
* Added a confirmation window before removing a Priority Ads configuration.
* Added Audit logs for Tiered Events.
* Added Audit logs for Segmentation.
* Added Audit logs for Shop.
* Added Audit logs for GDPR page.
* Added Audit logs for promotions.

###  01.02.2020 - 29.02.2020

* Fixed issues with the Graphana login (used for displaying the Graphs in the Console).
* Fixed issues with navigation regarding Virtual Goods Currencies and User Page.
* Changed the delete icon to a trash icon.
* Added additional events being tracked for the Advertising page.
* Added a loading indicator for Graphana graphs.
* Fixed file locations containing a leading slash if there is no path.
* Minor UI/UX fixes.
* Added default configuration download page.

###  01.01.2020 - 31.01.2020

* Refactored Devices Dashboard for the Event Dashboard.
* Removed unnecessary panels in the Game Dashboard.
* Fixed issue with permissions.
* Added Priority Ads for Interstitials.
* Refactored the Advertisement page to take into account Priority Ads.
* Changed all URL files to use paths.

<!-- tabs:end -->


