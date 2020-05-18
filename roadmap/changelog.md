---
description: View the latest changes to Sonoran CAD!
---

# Changelog

{% hint style="info" %}
_NOTE: All updates are released for Sonoran CAD Web, Windows Desktop, Android and iOS. Depending upon Google and Apple’s processing and review validation time, the latest Android and iOS application updates may not be available for up to 24 hours_
{% endhint %}

### 2.0.0 \(Full Release\) 5/16/2020

{% tabs %}
{% tab title="New" %}
1. Branding Logo
   * We've switched over to Sonoran CAD's new official logo!
2. API Endpoints:
   * Attach Units
   * Get Calls
   * Get Active Units
   * Unit Status
   * Kick Unit
   * New Dispatch
   * Remove Record
   * New Vehicle Registration
   * Edit Vehicle Registration
   * New License
   * Edit License
   * New Character
   * Edit Character
   * Remove Character
   * Get Characters
   * Check API ID
3. Server Push Events:
   * Unit Login
   * Unit Logout
   * Unit Status Update
   * Dispatch Event
   * Unit Call Clear
4. Integration Plugins
   * Call Commands
   * Check API ID
   * Live Map
   * Locations
   * Lookups
   * Postals
   * Push Events
   * Traffic Stop
   * Unit Status
   * Update Check
   * WraithV2
5. Page Transitions
   * All pages now have an improved smooth loading transition for a more refined user experience.
6. Vehicle Registration - Expiration Date
   * Added a vehicle registration expiration date field.
7. API Key - Generate New
   * Community owners can now request and generate a new API key in the admin menu.
8. Disconnection Banner
   * Server disconnection notices have been moved to a solid banner at the top of the screen.
9. UI Theme Changes
   * Updated UI layouts, accents, colors and more throughout the application.
10. Live Map - One Click Install
    * If your server uses the popular Live Map resource, you can now instantly configure and enable this all from within the admin panel. Sonoran CAD hosts your live map for you, so all you need to do is drag and drop our plugin into your resources folder.
{% endtab %}

{% tab title="Fixed" %}
1. Register - Same Username - Conflicting Keys
   * Fixed an issue where users could re-register the same username with a different email account after the expiration window. This caused user's to be unable to validate their user account.
2. Community Card
   * Fixed an issue where community cards with a wider aspect ratio would not properly expand down to fill the whole area in the community selection menu.
{% endtab %}
{% endtabs %}

### 1.22.0 \(Beta\) 5/07/2020

{% tabs %}
{% tab title="New" %}
1. Backend Migration
   * All backend and database services have been migrated over to a new docker container system with proper CI/CD integrations. A new development API path has been opened to work with community developers.
{% endtab %}

{% tab title="Fixed" %}
1. Register - Same Username - Conflicting Keys
   * Fixed an issue where users could re-register the same username with a different email account after the expiration window. This caused user's to be unable to validate their user account.
{% endtab %}
{% endtabs %}

### 1.21.1 \(Beta\) 5/01/2020

{% tabs %}
{% tab title="New" %}
1. Postal Code - Allow Letters
   * Postal code values in the call editor and department editor can now include letters for non-American communities.
2. Vehicle Registration - Unique Plate
   * Added a check to prevent users from creating a new vehicle registration with a license plate that already has a registration.
3. Email Expiration
   * Account verification emails are now properly invalidated and can be resent after 15 minutes.
{% endtab %}

{% tab title="Changed" %}
1. Active Calls - Order
   * Active dispatch calls now properly sort in descending order by default, with the latest calls at the top.
2. 911 Webhook - Geographic Customization
   * Changed the 911 Discord webhook information to "Emergency" for non-American communities.
3. Rate Limits - Increased
   * Increased internal websocket rate limits to help prevent users from being temporarily blocked with false positives.
{% endtab %}

{% tab title="Fixed" %}
1. Email Address - Space
   * Added additional server side checks to prevent users from registering an email with a space.
2. Record Wipe - Error Message
   * Fixed an issue where the error message for non community owners trying to wipe records would not display.
3. Identifier - Blank
   * Added a new check to set unit numbers to 'NOT SET' to prevent an issue where entirely blank units would be displayed improperly.
4. Unban User - Wording
   * Fixed an issue where the confirmation prompt for unbanning a user was still phrased as 'Ban User'
{% endtab %}
{% endtabs %}

### 1.21.0 \(Beta\) 4/22/2020

{% tabs %}
{% tab title="New" %}
1. Global Configurable Hotkeys
   * All web and desktop users can now configure hotkeys for panic and unit status changes. Global hotkeys are also supported in the desktop application and will trigger regardless of whether or not the application is visible and focused.
2. PDF - Caps
   * Forced all PDF text fields to capitalized text. This aids in consistency between the displayed values in the record editor and exported PDF documents.
3. Discord Webhooks - Caps
   * Forced all Discord record fields to capitalized text. This aids in consistency between the displayed values in the record editor and Discord webhook notifications.
{% endtab %}

{% tab title="Fixed" %}
1. Remember Me - Changed ID
   * Fixed an issue where logging into your default community would produce an error message if your community has recently changed their ID.
2. Lawyer - Civ
   * Fixed an issue where layers could not properly open or view civilians in a records search.
3. PDF - Date
   * Fixed an issue showing the officer's name label in the PDF agency section as 'Date'
{% endtab %}
{% endtabs %}

### 1.20.4 \(Beta\) - 4/19/2020

{% tabs %}
{% tab title="New" %}
1. Community ID - Change
   * Community owners can now change their community ID in the admin panel.
2. Admin - Wipe Records
   * A CAD wipe can be initiated in the admin panel and can be configured to remove all specified record types.
3. Admin - Tutorials
   * Added a new tutorials button in the admin menu and updated existing tutorial links.
{% endtab %}

{% tab title="Changed" %}
1. Admin Menu - Buttons
   * Updated all admin panel refresh and other buttons to a more consistent styling.
{% endtab %}

{% tab title="Fixed" %}
1. Incoming 911 TTS
   * Fixed an issue causing the "Incoming 911" TTS notification from not playing properly.
2. Version Check - Blank Version
   * Added additional error handling to the version check notification to prevent an issue displaying the notification with the latest version for some users.
3. Community ID - Overlap
   * Fixed an issue causing the community ID badge in the side menu to overlap onto the page for communities with a long ID.
4. Desktop - External Links
   * Fixed an issue where opening the external tutorial site in the desktop app would not open a new browser window.
5. Civilian - Exit Editor
   * Fixed an issue where closing the civilian character editor would swap your currently selected character back to the first character, and not the existing one a user had selected.
{% endtab %}
{% endtabs %}

### 1.20.3 \(Beta\) - 04/17/2020

{% tabs %}
{% tab title="New" %}
1. Admin - Ownership Authentication
   * Added a new feature for owners of the community to retrieve a unique key to prove ownership. This aids in authenticating users in support tickets, for manual requests particularly in our upcoming customer support app.
2. Side Bar - Community ID
   * Added a small badge to display the current community ID in the side navigation bar. This aids in support questions.
3. Side Bar - Tutorials
   * Added a navigation button to our new guides and tutorials site in the side bar menu.
4. Version Check - UI
   * Added a new popup to inform users if they are running an outdated version of Sonoran CAD.
{% endtab %}

{% tab title="Changed" %}
1. Easter Egg - Removed
   * Removed a voice command Easter egg discovered by users.
{% endtab %}

{% tab title="Fixed" %}
1. Penal Code - Configuration
   * Fixed an issue where new or updated penal codes were not reflected until a page refresh.
{% endtab %}
{% endtabs %}

### 1.20.2 \(Beta\) - 04/15/2020

{% tabs %}
{% tab title="Fixed" %}
1. Electron Uninstaller - Warning
   * Fixed an issue with the latest NSIS uninstaller for the desktop app that caused a false positive with Windows Defender.
2. Admin - Penal Codes
   * Fixed an issue where penal codes would not populate in the admin menu.
3. PDF - Charge Number
   * Fixed an issue causing the charge numbers in PDF records to be zero based instead of one based.
4. Warrant - Closed
   * Fixed an issue causing closed warrants to still be announced over TTS.
5. BOLO - Active
   * Fixed an issue causing closed warrants to still display locally for users in the active warrants window when closing the record.
{% endtab %}
{% endtabs %}

### 1.20.1 \(Beta\) - 04/13/2020

{% tabs %}
{% tab title="New" %}
PDF Print - Mobile

* PDF printed records are now accessible on mobile.

BOLO - PDF

* BOLO records can now be printed to PDF format.

Vehicle Registration - PDF

* Vehicle registration records can now be printed to PDF format.

License - PDF

* License records can now be printed to PDF format.

PDF Records - File Name

* PDF downloaded records and call logs now have a proper file name when saving.

Character DOB - Age

* Character age now properly auto-calculates consistently when changing your character's DOB.
{% endtab %}

{% tab title="Fixed" %}
Call History

* Fixed an issue causing call history to pull the oldest closed calls instead of the most recent.

DMV Record - New

* Fixed an issue where civilians could not edit their initial vehicle registration information without the DMV add or edit permission.

Vehicle Citation - Pace Type

* Fixed an issue causing the vehicle citation pace type dropdown to be blank.

New BOLO - TTS Undefined

* Fixed an issue where a new BOLO audio alert would list the name and plate as undefined.

Warrant Status

* Fixed an issue causing warrant statuses to not be properly saved.

DMV - Pending Records

* Fixed an issue causing pending records to not be shown properly in the DMV pending section.

PDF Records - Desktop

* Fixed an issue causing PDF record downloads to be blank in the desktop application.
{% endtab %}
{% endtabs %}

### 1.20.0 \(Beta\) - 04/12/2020

{% tabs %}
{% tab title="Changed" %}
Records System - Backend Restructure

* The records structure and storage system has been completely overhauled to be more efficient and consistent. This also makes way for future API calls for record lookups.

DBSync - Character Hide ID

* Character ID \(often Steam IDs\) are no longer displayed on the UI when searching for a character with database sync. 

Dispatch - Clear Panic Permissions

* Fixed an issue where dispatchers could not clear a unit's PANIC state if they did not have police, fire, or EMS permissions.

DBMerge - Client Disable Check

* The database merge toggle is now properly disabled client-side to avoid false security warnings.

New Record - BOLO

* BOLO record creation has been moved to the standard new record section.
{% endtab %}

{% tab title="Fixed" %}
Penal Code - Freeze

* Fixed an issue causing some browsers to freeze, lag, or become unresponsive with multiple penal code windows open at once.

Penal Code - Remove Wording

* Fixed the incorrect phrasing when removing a penal code.

Penal Code - Empty Bond

* Fixed an issue causing records to not save if a penal code bond amount or charge count was removed and left empty.
{% endtab %}
{% endtabs %}

### 1.19.1 \(Beta\) - 04/05/2020

{% tabs %}
{% tab title="New" %}
Record Flags - Customize

* Communities can customize their record flag types.
{% endtab %}

{% tab title="Changed" %}
Pricing Page - Redesign

* Improved and updated the pricing page with more information.
{% endtab %}

{% tab title="Fixed" %}
Self-Dispatch - Calls

* Fixed an issue causing the active calls and call history to not load properly for units in self-dispatch mode.
{% endtab %}
{% endtabs %}

### 1.19.0 \(Beta\) - 04/04/2020

{% tabs %}
{% tab title="New" %}
Call History

* Previously closed calls can now be viewed for record purposes.

Call History - PDF Print

* Calls in the call history section can now be exported to a PDF record.

Lawyer Page

* Users with the lawyer permission can lookup all records on a name or plate in the lawyer page.

Voice Customization

* Users can now change the text-to-speech voice in the settings popup.

Active Calls - Close

* You can now also close a dispatch call by clicking the call in the active calls window, and selecting "Close Call"

Call ID

* Dispatch Call IDs are now displayed in the active calls list as well.
{% endtab %}

{% tab title="Fixed" %}
Unit Group - Status Change

* Fixed an issue where a unit in a unit group changing their status would change the status of all unit groups.

Character DOB - Disabled

* Fixed an issue preventing non Database Sync communities from editing the civilian DOB field.

Dispatch - Preview Call

* Fixed an issue where dispatchers could not properly preview a call on the active calls list.

Dispatch - Signal

* Fixed an issue where an active signal would not be displayed for dispatchers first loading the page.
{% endtab %}
{% endtabs %}

### 1.18.0 \(Beta\) - 03/30/2020

{% tabs %}
{% tab title="New" %}
Database Merge

* Database merge can now be enabled in the in-game integration panel for Pro communities. This allows you to save additional information in records not provided by your in-game database. This additional data will be stored by Sonoran and merged with your Database Sync records.
{% endtab %}

{% tab title="Changed" %}
Custom Login - Header Branding

* The custom login page now displays your community name in the top header instead of "Sonoran CAD"
{% endtab %}

{% tab title="Fixed" %}
1. DbSync Character Gender
2. Fixed an issue where database sync character genders wouldn't be properly displayed.
{% endtab %}
{% endtabs %}

### 1.17.1 \(Beta\) - 03/28/2020

{% tabs %}
{% tab title="New" %}
1. Call Preview
2. You can now open an additional pop-out window to preview a call without having to self-attach or open it in your existing editor.
{% endtab %}

{% tab title="Changed" %}
1. Penal Code: Fine Amount
2. Made the penal code "Bond/Fine Amount" wording consistent in the admin panel and charges section in records.
{% endtab %}

{% tab title="Fixed" %}
1. 10-Codes: Empty
2. Fixed an issue where 10-codes in the popout window would not display properly for units.
3. Active Calls - 10-Code
4. Fixed an issue causing the active calls table from not properly displaying the new 10-code format.
{% endtab %}
{% endtabs %}

### 1.17.0 \(Beta\) - 03/00/2020

{% tabs %}
{% tab title="New" %}
10-Codes: Redesign

* The 10-Code system has been overhauled to be much more simplistic and customization. You can now more quickly enter in 10-Codes in the new admin UI. All 10-Codes are entered solely as text to no longer limit communities who do not use 10-Codes.

Penal Codes - Custom Bond and Charge Types

* Communities can now customize the penal code bond and charge type values to be selected from. This allows communities outside the US, or communities that do not use the standard penal code type and bond options to specify these values.

Dispatch - 10-Code

* 10-Codes are no longer required to create a dispatch, and do not have to be entered as a specified 10-Code from the admin page.

Server Mode - European/UK

* The admin customization menu now allows you to toggle your community's geographic settings. Changing from American to European will rephrase 911 to 999 and more!
{% endtab %}

{% tab title="Fixed" %}
1. Custom Login Page - Add Account
2. Fixed an issue where creating a new account from a custom login page would not automatically add their account to the community,
3. Voice Commands - Custom Status
4. Fixed an issue where voice commands to change a unit's status code would not work with customized status options.
5. Arrest Record - DBSync Vehicle
6. Fixed an issue where arrest reports with a database sync vehicle added could cause the record to not save if the vehicle type was not specified.
{% endtab %}
{% endtabs %}

### 1.16.0 \(Beta\) - 03/24/2020

{% tabs %}
{% tab title="New" %}
Unit Grouping

* Units can now be grouped together to more easily dispatch units riding together.

New Unit - Editor

* Loading in the Police, Fire, or EMS page for the first time will auto-open the unit editor to help users set their initial unit information more quickly.

Civilian - Limit Characters

* Communities can now set a limit on how many characters each account can have.

Civilian - Limit Licenses

* Communities can now limit the number of licenses a single civilian can have.

Civilian - Limit Vehicles

* Communities can now limit the number of vehicle registrations a single user can have.

Session Invalidate - UI

* The session expiration/invalidation and invalid cookies alert is now a built-in UI element that will navigate the user back to the login page, as opposed to a standard web alert.
{% endtab %}

{% tab title="Changed" %}
1. Rate Limit - Increase
2. Rate limit values have been increased to prevent blocking users with a legitimate higher frequency of requests.
3. Custom Login Page - Query Strings
   * In order to reduce the strain on Sonoran CAD's servers, all custom login pages must now specify multiple attributes as query strings. You can copy and paste the entire URL from the Custom Login Page section in the Admin Customization menu.
4. Custom URL - Format
5. Custom login URLs are now more properly generated to replace any spaces with the %20 value.
6. Custom Login - Email Query Strings
7. Updated the create account and forgot password URL generators to include all the query strings for a custom login page if the user creates a new account or resets their password on a custom login page.
{% endtab %}

{% tab title="Fixed" %}
1. Unit Login - Active
2. Fixed an issue where units would not show in the active units window for the local user.
3. Dispatch Login - Active Unit
4. Fixed an issue causing dispatchers to display as an online unit.
5. General Citation - Save
6. Fixed an issue where saving/updating an existing general citation causes the database to set the last name as the first name. The record was saved in the database as "First First" even though the data in the record was "First Last".
7. General Citation - Count
8. Fixed an issue causing the general citation tab count to display the wrong number.
9. DBSync - Remove Character
10. Fixed an issue where users could not un-link a database sync character.
{% endtab %}
{% endtabs %}

### 1.15.2 \(Beta\) - 03/22/2020

{% tabs %}
{% tab title="New" %}
1. Websocket Optimization
   * Started large improvements for backend service websocket calls to help reduce strain on our servers.
2. Rate Limiting - UI and Blacklist
   * A new in-depth rate limiting system ensures users do not abuse backend endpoints, displays convenient UI notifications, improves security, and more.
{% endtab %}
{% endtabs %}

### 1.15.1 \(Beta\) - 03/18/2020

{% tabs %}
{% tab title="New" %}
1. Custom Login Page - Query Strings
   * In order to reduce the strain on Sonoran CAD's servers, all custom login pages must now specify multiple attributes as query strings. You can copy and paste the entire URL from the Custom Login Page section in the Admin Customization menu.
2. Edit Unit - Permission Label
   * Changed the edit identifier label to have the same label name on both account permissions and permission keys. 
{% endtab %}

{% tab title="Fixed" %}
1. Community Branding
   * Fixed an issue where plus communities had branding removed in the top header instead of Pro communities.
2. Community Card - Subtitle Overflow
   * Fixed an issue where communities with a long subtitle value would overflow on the community card. The subtitle now properly cuts off with an ellipsis.
3. DMV Permission
   * Fixed an issue where DMV record statuses could not be edited in the civilian page without the DMV page permission.
4. Lua Resource - Download Links
   * Fixed an issue where the Lua Resource download buttons in the admin panel downloaded the outdated files instead of the latest GutHub release. 
5. API Tutorial - Download
   * Fixed an issue where some tutorial video links were downloads for desktop application users.
6. Record Add Vehicle - Plate Search
   * Fixed an issue where searching for a vehicle to add to a record would not work if searching by the plate number.
7. DMV - Database Sync
   * Fixed an issue where license and vehicle registration searches in the DMV page would return no or limited results for communities with database sync.
8. Database Sync - Civilian Link
   * Fixed an issue where you could not view your database sync linked characters unless you also had license or vehicle registration mapping enabled as well.
{% endtab %}
{% endtabs %}

### 1.15.0 \(Beta\) - 03/04/2020

{% tabs %}
{% tab title="New" %}
1. In-Game /911 and /311
   * Our easy to install integration script now also includes a /911 and /311 command to send emergency and non-emergency calls directly to your dispatchers!
2. Multiple Servers
   * Communities can now configure multiple "servers" in their CAD. This is for communities that have more than one server. All active units and dispatching is kept separate between servers, but all records are shared. To change your server, users can select the server from the drop-down in the top left.
3. Unit - Self Clear
   * Units can now remove themselves from their active dispatch call.
4. Pricing Page
   * A new pricing page helps our team direct users to the most up to date pricing and feature information.
5. Inactive Communities
   * Communities that have no one sign in for 30 days will be automatically removed from the database.
6. Custom Login Page - Instructions
   * The custom login page section now includes additional instructions, informing users to enter their community ID into the index.html file.
7. Database Sync - Tutorial
   * Added a database sync tutorial link in the admin panel.
8. Self Dispatch - Permission
   * Self dispatching is now a permission separate from the dispatch permission.
9. Webhook - Tutorial
   * Added a webhook tutorial link in the admin panel.
10. Permission Key Applied - Notice
    * When a permission key is correctly applied, the user is now notified with an alert.
11. Community Customization - Tutorials
    * Added PDF tutorial links in the community customization menu for query strings and voice command options.
{% endtab %}

{% tab title="Changed" %}
1. Empty Lookup
   * Prevented users from running a blank/empty police or records lookup.
2. Invalid Permissions - Error
   * Included more details into a missing permissions security error.
3. Community Limit - Error
   * Added more detail in community limit reached errors from the server side.
4. Signal - Numeric Check
   * Signal values can now only be a numeric value of up to 4 digits.
5. Header - Community Name
   * Changed the header formatting to ellipsis to better accommodate for long community names.
6. Nav Bar - Version
   * The application version number is now displayed in the bottom of the side navigation menu.
7. Community Card - Ellipsis
   * Changed community card title/header to cut off into an ellipsis if the name is too long. This prevents the remove icon from being bumped down to the next line.
8. Civilian Card - Header
   * Forced all civilian card headers \(name\) to be capitalized.
9. Privacy Policy - Login Only
   * The privacy policy button only displays in the side nav bar on the login screen. This helps reduce clutter on the community pages.
{% endtab %}

{% tab title="Fixed" %}
1. Ban User
   * Fixed an issue where user could not be banned, as the backend was incorrectly checking that the user being banned was the community owner and not the other way around.
2. Dispatch Note - Webhook
   * Fixed an issue where dispatch call notes were not shown in Discord webhooks.
3. Lookup - Civilian
   * Fixed an issue where the civilian results on a lookup would not show unless a regular record was also shown.
4. Call Closed - Notes
   * Fixed an issue where the call notes would still be displayed when a call was closed.
5. Call Notes - Disable
   * Fixed an issue where call notes could be added when the unit does not yet have an active call.
6. Add Note - Button Width
   * Fixed an issue where the "Add Note" button on the call editor wouldn't take up the full space for mobile devices.
7. Civilian - DMV Records
   * Fixed an issue causing civilians to need the DMV Record Add permission to apply for a new DMV record with the default "PENDING" status. Civilians can now properly apply for a DMV record if they do not have the explicit DMV add record permissions.
8. Civilian Records - Lookup
   * Fixed an issue where civilians could not view their records if they did not have the police or dispatch permission enabled.
9. Transfer Community - Permissions
   * Fixed an issue where transferring ownership of a community did not grant the new owner the new self dispatch and edit other unit permissions.
10. Permission Change - Webhooks
    * Fixed an issue causing the permission change webhook from not showing the newer advanced permissions.
11. Failed Payment
    * Fixed an issue where subscription charges that failed would still bump the subscription expiration date by another month.
12. Call Note - Self Dispatch
    * Fixed an issue where adding a new call note would show an additional active dispatch call for users in self-dispatch mode.
{% endtab %}
{% endtabs %}

### 1.14.0 \(Beta\) - 02/16/2020

{% tabs %}
{% tab title="New" %}
1. Dispatch - Signal
   * Dispatchers and users in self-dispatch mode can now put the server into a custom signal status. Ex: Signal 100
2. Dispatch - Live Editor
   * If a dispatcher has the call editor open and the call is updated by someone else, this will live-update their editor as well.
3. Timezone
   * All clock values in Sonoran CAD are now synced based upon your community's set timezone. By default, this is UTC time. This can be customized in: Admin &gt; Customization &gt; Community Info
4. Dispatch Call - Notes
   * All dispatch calls now have a notes section. Notes can be added using the input section below, and will be auto formatted with a timestamp and unit number.
5. 911 Call - Autoremove
   * 911 calls are now automatically removed from the queue when you create a dispatch call after selecting "View In Editor"
6. Record - Charge Total
   * All charge/fine totals are calculated for an easy reference at the top of the charges section.
7. Permissions - Guide
   * Added a permissions guide to the account permission and permission key modal.
8. Permissions - Guide
   * Added a permissions guide to the account permission and permission key modal.
9. Self Dispatch - Permission
   * Self dispatching is now a permission separate from the dispatch permission.
10. Edit Other Identifier - Permission
    * A new permission has been added to separate the ability to edit your own identifier, and edit someone else's identifier.
11. Permission Key Applied - Notice
    * When a permission key is correctly applied, the user is now notified with an alert.
12. Penal Code - Sorting
    * Penal codes now sort better, to include codes with integers with more than 1 digit.
13. Support Page
    * Added a new support direction page per Apple's application standards/requirements.
{% endtab %}

{% tab title="Fixed" %}
1. Charges - Edit
   * Fixed an issue preventing users from modifying charge information on a new record.
2. Civilian - Records
   * Fixed an issue causing the civilian page records to not show when searched.
3. Panic - Unit Number
   * Fixed an issue causing PANIC webhooks to not display the unit number.
4. Status Change - Permissions
   * Fixed an issue causing units to not be able to change their status if they did not have the "Police Edit Unit" permission enabled.
5. Account Join - Duplicate
   * Fixed an issue causing the error message when joining a community you are already in from being a message to contact support.
6. Police Search DMV - Permissions
   * Fixed an issue where police could not search for a civilian character or vehicle registration when filling out a record if they did not have DMV permissions.
7. Live Map - Height
   * Fixed an issue where the live map would be displayed in only the top portion of the popout window.
8. Community Card
   * Fixed an issue where the community card could not be selected if the community image did not load for some reason.
9. API Fail - JSON
   * Fixed an issue where failed API calls would not properly return the original JSON body/request object passed in.
{% endtab %}
{% endtabs %}

### 1.13.X \(Beta\) - 02/09/2020

{% tabs %}
{% tab title="New" %}
1. Unit - Self Dispatch
   * Units with dispatch permissions can now enable "Self Dispatch"

     Self dispatching allows you to create a call, edit your existing call, or attach yourself onto an existing active call.
2. Lookup - Civilian ID
   * When running a lookup, all applicable civilian ID information will also be displayed.

Window - Dynamic Height

* Popout windows now resize to a dynamic height much more efficiently. This also greatly improves the mobile user experience.

API Fail - JSON

* API failure webhooks now also return the original JSON message to better aid in debugging. API Keys are also censored.

Name Formatting - Dynamic

* Names are displayed with dynamically calculated formatting. This prevents a comma being displayed after the last name if it does not exist, and a period being displayed after the middle initial if it does not exist.

Compare Plans - Pricing

* Subscription pricing amounts are now displayed in the "Compare Plans" window.
{% endtab %}

{% tab title="Fixed" %}
1. BOLO - Penal Code Section
   * Fixed an issue preventing the penal code/charges section on BOLOs to not properly display.
2. DB Sync - Search Characters
   * Fixed an issue where using database sync to search for characters would fail if license or vehicle mapping was not enabled.
3. Transfer Community - Email
   * Fixed an issue where the transfer community feature would fail when the email template could not be located.
{% endtab %}
{% endtabs %}

### 1.12.0 \(Beta\) - 02/04/2020

{% tabs %}
{% tab title="New" %}
1. BOLO Window - Warrants
   * The BOLOs window will now also let you search and view all active warrants.
2. Webhook - 911
   * Discord webhooks can now be sent when a 911 call is received.

Email Subject - Customize

* Customized community emails now also display your custom community name in the subject line.

Vehicle Type - Aircraft

* "Aircraft" has been added as a vehicle registration type.

Active Units - Panic

* Regular units can toggle another unit's PANIC status with the proper permissions.

  Active Units - Kick

* Regular units can now kick other units in the active units window if they have the proper permissions.

API Fail - Error Catching

* Added further detail for failed API calls. These details will be displayed in API failed webhook notifications.

Dispatch - 10-Codes Sort

* Dispatch 10-codes are now sorted in order before being filtered by textbox input.

Rate Limiting - Security

* To better combat the recent string of cyber attacks, new rate limiting features have been implemented on Sonoran CAD’s website, websocket connections, and API requests.
{% endtab %}

{% tab title="Changed" %}
Dispatch - Postal/Address

* Dispatch calls no longer require an address or postal to be created.

Ban - Check Owner

* Community owners can no longer ban themselves.
{% endtab %}

{% tab title="Fixed" %}
1. Civilian DMV Edit
   * Fixed an issue where civilians could not edit or remove DMV records if they had DMV edit or remove permissions, but did not have DMV page access.
2. Volume - Null
   * Fixed an issue where the default volume would be an undefined value. This prevented users on the desktop app from changing their status.
3. DbSync - Record Actions
   * Fixed an issue where the record action bar would still display for read-only records via database sync.
4. Compare Plans - Departments
   * Fixed an issue where the compare plans department numbers were incorrectly lower.
{% endtab %}
{% endtabs %}

### 1.11.4 \(Beta\) - 01/30/2020

{% tabs %}
{% tab title="New" %}
1. Query String - Mute Audio
   * Added a query string to set the default audio volume for communities embedding the CAD inside of a resource.
{% endtab %}

{% tab title="Fixed" %}
1. Admin - Accounts
   * Fixed an issue where navigating away from the admin panel's accounts section would fail to show user accounts when navigating back.
2. Custom Login - New Account
   * Fixed an issue where joining a new community for the first time using a custom login page would fail, resulting in a banned user and account permissions error.
3. Search Character - DbSync
   * Fixed an issue where police and dispatch did not pass permission checks when searching for a civilian character in database sync.
4. Change Username - Error
   * Fixed an issue causing a username switch to throw an error if a member did not have any owned or member communities.
{% endtab %}
{% endtabs %}

### 1.11.3 \(Beta\) - 01/30/2020

{% tabs %}
{% tab title="New" %}
1. DbSync - JSON Key
   * Communities that have a JSON field can now specify the a key in the column containing the value. The DbSync tutorial document covers this new SQL syntax in section 1.5 \(Advanced\).
2. Query String - Force Mobile
   * sonorancad.com/\#/?forcemobile=TRUE

     Your CAD will forcefully format the emergency services action bars to mobile format. This is beneficial for communities that are embedding the CAD in-game on a smaller format that does not quite meet the standard mobile dimensions.
{% endtab %}

{% tab title="Changed" %}
Downloads - iOS App

* Updated the iOS app store download link on the downloads page.

UI Border

* Remove the green border from emergency page sections.
{% endtab %}

{% tab title="Fixed" %}
1. Custom Login - New Account
   * Fixed an issue where user accounts were not properly generated when joining a new community from the custom login screen.
2. Vehicle - DbSync
   * Fixed an issue where vehicle attribute textboxes were still enabled for editing when viewing database sync records.
3. Community Branding
   * Fixed an issue where the Sonoran CAD branding would not be removed for PRO communities.
4. Display - Rotate
   * When rotating the display from portrait to landscape, record lookup results will fail to display.
{% endtab %}
{% endtabs %}

### 1.11.2 \(Beta\) - 01/28/2020

{% tabs %}
{% tab title="New" %}
1. Ban System
   * A new ban system has been implemented to more easily view, add, and remove banned users. This system also comes along with improved security checks to prevent banned users from accessing your community,
2. Webhook - Ban
   * Webhooks are now received when a user is banned or unbanned.
3. Account Status
   * The user accounts table now allows you to quickly filter user accounts by their status: Pending, Active, or Banned.
4. PANIC - Webhook
   * The PANIC webhook now also includes the unit's location.
5. PANIC API - Webhook
   * PANIC webhooks are now also sent out when sent via web API.
{% endtab %}

{% tab title="Fixed" %}
1. Join Community
   * Fixed an issue where users could not search and join a community ID.
2. Fire & EMS Call Viewer
   * Fixed an issue where the Fire and EMS call viewer would still show some default data when no call is present.
3. Fire & EMS - Retrieve Call TTS
   * Fixed an issue where the fire and EMS page would state a null dispatch text to speech when first loading.
4. PANIC Webhook
   * Fixed an issue causing the unit PANIC webhook to use the identifier's unique database ID instead of the unit number.
5. Civilian DMV - Apply for License
   * Fixed an issue where the civilian DMV record page would fail to display the "Apply for DMV Record" button for users who do not have the permission to add a new DMV record.
{% endtab %}
{% endtabs %}

### 1.11.1 \(Beta\) - 01/25/2020

{% tabs %}
{% tab title="New" %}
1. Community Selection - Redesign
   * The community selection menu has been completely redesigned for a much better mobile UI experience and look.
2. Privacy Policy
   * A standard privacy policy has been added to the side navigation drawer per Apple's standards.
{% endtab %}

{% tab title="Changed" %}
1. Loading Icon - Mobile
   * Redesigned a more dynamically calculated loading icon system. This icon fits more properly for mobile devices.
2. Login Page - Mobile
   * Improved the login screen UI for mobile users.
3. Community Menu - Mobile
   * Mobile UI improvements to the community menu page.
{% endtab %}

{% tab title="Fixed" %}
1. BOLO - Modify
   * Fixed an issue where BOLOs could not be properly removed or modified.
{% endtab %}
{% endtabs %}

### 1.11.0 \(Beta\) - 01/25/2020

{% tabs %}
{% tab title="New" %}
1. 911 System
   * Allow civilians to create 911 calls to be displayed to dispatchers.
2. 911 API
   * 911 calls can now be sent via Sonoran CAD's web API from in-game.
{% endtab %}

{% tab title="Changed" %}
1. Unit PANIC
   * Unit PANIC now utilizes the faster panic method used in API calls.
2. Switch Identifier
   * Units are prevented from switching their identifier on the UI if they do not have the edit unit permissions.
{% endtab %}

{% tab title="Fixed" %}
1. General Citations - New
   * Fixed an issue where adding a general citation would fail.
2. DB Sync - Case Sensitivity
   * Fixed an issue where database sync searches would still be case sensitive for some communities if their database did not support a particular case sensitivity syntax.
3. Identifier - Edit
   * Fixed an issue where dispatchers and units could not edit other user's identifiers, and unit statuses would not be populated properly in the unit editor.
4. Panic Undefined - Dispatch
   * Fixed an issue where unit PANICs would state "Undefined" for dispatchers.
5. PANIC - Toggle
   * Fixed an issue where units could not properly toggle their PANIC status off if their unit did not have a department set.
{% endtab %}
{% endtabs %}

### 1.10.4 \(Beta\) - 01/22/2020

{% tabs %}
{% tab title="New" %}
1. Page Loader - Branding
   * The page loader now displays your custom community logo.
2. Limits - Version and Expiration
   * The community limits section now displays your community's current subscription version and expiration date.
{% endtab %}

{% tab title="Changed" %}
1. Community Menu - Loading
   * The community menu now properly has a loading transition. This makes the page no longer snap as permissions are loaded.
2. Civilian & DMV - Icons
   * Updated civilian and DMV page icons to the newer style.
3. Dispatch - Loading
   * The dispatch page now properly has a loading transition. This makes the page no longer snap as permissions are loaded.
4. Tab Bottom Border - Mobile
   * Removed the dotted bottom border on tabs for mobile users.
{% endtab %}

{% tab title="Fixed" %}
1. Call Editor - Mobile
   * Fixed an issue where the call editor's "Address" input would not stretch all the way across the screen for mobile users.
2. API Key - Display
   * Fixed an issue causing the community API key to not display on the in-game integration page.
{% endtab %}
{% endtabs %}

### 1.10.3 \(Beta\) - 01/22/2020

{% tabs %}
{% tab title="New" %}
1. Themed Scrollbar
   * A new customized scrollbar fits the dark CAD theme better for a much more app-like feel.
2. API Scripts
   * Added a download button to the current .lua in-game integration script in the Admin page's "In-Game Integration" panel.
{% endtab %}

{% tab title="Changed" %}
1. In-Game Integration Config Layout
   * Greatly improved the layout of the in-game integration panel with drop-downs and other mobile UI improvements.
2. Discord Webhook Config Layout
   * Greatly improved the layout of the Discord webhook panel with drop-downs and other mobile UI improvements.
3. Sidebar - Download and Fullscreen
   * The download and fullscreen button no longer displays for users on an app or PWA installation.
4. Admin - Panel Widths
   * Admin panels now span across the entire page regardless of the screen size.
5. Color Customization - Padding
   * Added padding and background color to the page color customization boxes.
6. Added padding to the page color customization boxes.
   * Tabs now display properly on the bottom of the actions container. Close button styling has been modified to be smaller and more precisely placed.
7. Sidebar - Common Buttons
   * Common buttons in the sidebar like logout, settings, etc. are now displayed at the bottom of the navbar.
8. Icons - Consistency
   * Changed icons in the record viewers, BOLO window, admin sections, etc. to the "outlined" version for more consistency.
9. BOLO - Charges
   * Updated the BOLO record charges section to the standardized charges section used in arrest, warrant, and general citation records. This greatly improves the mobile UI experience.
10. No Permission Keys - Error Message
    * Changed the server error message when a community has no permission keys to the standard "Invalid Permission Key" error instead of warning that "NULL" permission keys were found.
{% endtab %}

{% tab title="Fixed" %}
1. Record Windows
   * Fixed an issue where record and other window popups would fail to open.
2. Record Action - Mobile
   * Fixed an issue where action buttons on a record would be moved down to another line on mobile and wouldn’t be fully accessible.
3. Set Default Community - Display
   * Fixed an issue where pressing "Set Default Community" at the community menu failed to immediately hide the button after being toggled.
4. Record Window - Mobile
   * Fixed an issue causing the new record data section to not display properly on certain mobile device screen sizes.
{% endtab %}
{% endtabs %}

### 1.10.2 \(Beta\) - 01/21/2020

{% tabs %}
{% tab title="New" %}


1. Panic - Location
   * Unit PANIC text-to-speech alerts now state the unit's location
2. BOLO - Agency Information
   * BOLO agency information now properly auto-fills with the identifier's information.
3. Unit Location - API
   * API call to show a unit's location in real time in the unit section.
4. Compare Plans - Description
   * Added an information tooltip next to each feature in the "Compare Plans" popup in the payment center.
{% endtab %}

{% tab title="Changed" %}
1. DMV Record - Search
   * The search button for characters and vehicles in the DMV record will only display on DMV records if the user has the DMV page access permission.
{% endtab %}

{% tab title="Fixed" %}
1. BOLO - WebHook
   * Fixed an issue causing BOLO webhooks to not be properly sent.
2. API Webhook - Label
   * Fixed the wording on the new API webhook to properly display as "API Request" instead of a duplicate of "Penal Code Modified"
{% endtab %}
{% endtabs %}

### 1.10.1 \(Beta\) - 01/19/2020

{% tabs %}
{% tab title="New" %}
1. Unit Info - Identifiers
   * Units can create and save multiple unit identifiers. These can then be quick selected and changed.
2. Dispatch - Identifiers
   * Dispatchers can configure their current unit identifier to more quickly generate new records.
3. Unit Location - API
   * API call to show a unit's location in real time in the unit section.
4. Panic - API
   * Unit's can have their PANIC status toggled via an API request.
5. Unit Info - Location and AOP
   * Unit identifiers can now specify their current location and AOP. 
6. Custom Emails
   * Customize branding and wording in emails sent from your custom login page. This includes account verification/creation and forgotten password emails.
7. Custom Page Colors
   * Communities can now specify the background colors of their custom login page or community menu page.
8. Sonoran CAD Branding
   * Professional communities have their community name displayed on the top left instead of the Sonoran CAD name.
9. Webhook - API Request
   * Discord webhooks can be enabled for successful and failed API requests.
10. Customization Menu - Expandable
    * Added a new expandable section system to the community customization menu. This allows for a more condensed and organized page.
{% endtab %}

{% tab title="Changed" %}
1. Dispatch Call Overhaul
   * Completely overhauled how dispatch calls are stored, retrieved, and modified. This system is much more optimized and will allow for expansion into viewing previously closed calls and adding in 911 calls in the near future.
2. Police/Fire/EMS UI Changes
   * Small UI changes for emergency pages related to styling, spacing, etc.
3. Dispatch - Description
   * A call description is no longer required for dispatches.
4. Record View - DBSync
   * Record views no longer display the "Search" buttons for characters and vehicles when database sync is enabled, as this data is read-only.
5. DMV Records - Search
   * The button to search for a vehicle or civilian character will no longer display on a license or vehicle registration if you do not have permissions to add, edit, or remove the record.
6. Emergency Action Buttons - Mobile
   * Emergency action and PANIC buttons are now smaller to match the size of the status buttons on mobile devices.
7. Default Community - Hide
   * The "Set Default Community" button will no longer display at your community menu if the community is already set as your default.
8. Permission Keys - Spaces
   * Added a check to prevent users from adding a space in a permission key.
9. Emergency Clock - Mobile
   * The clock on all emergency pages no longer displays for mobile screens in order to save space.
{% endtab %}

{% tab title="Fixed" %}
1. Permission Keys - Error
   * Fixed an issue where error messages were not sent if an invalid permission key was applied.
2. Edit Unit - Status
   * Fixed an issue where changing your unit status through the unit editor would always set it to unavailable.
3. Fullscreen - Scrollbar
   * Fixed an issue where the scrollbar would display unnecessarily when in full screen mode on desktop.
{% endtab %}
{% endtabs %}

### 1.9.7 \(Beta\) - 01/12/2020

{% tabs %}
{% tab title="New" %}
1. Default Community
   * Users can now locally set their "Default Community" in the community menu. This will always display the community's custom login screen even for mobile and desktop applications. This makes signing into your regular community even faster!
2. Admin - Kick Account
   * Community admins can now kick an account to forcefully remove it from a community as opposed to banning the account. 
{% endtab %}

{% tab title="Changed" %}
1. Login Page - Icons
   * Small changes to the login page icons and button sizes.
{% endtab %}

{% tab title="Fixed" %}
1. Admin - View Accounts
   * Fixed an issue where navigating from another admin panel back to the user accounts page caused the accounts to be empty until refreshed.
{% endtab %}
{% endtabs %}

### 1.9.6 \(Beta\) - 01/11/2020

{% tabs %}
{% tab title="New" %}
1. Custom Login Page
   * Communities can customize their own login page to display their community name and logo. Users logging in from this page will be directly logged into the community, as opposed to navigating to the community selection menu. All account creation and password recovery emails sent from this page will also navigate the user to your community's custom login page.
{% endtab %}
{% endtabs %}

### 1.9.5 \(Beta\) - 01/11/2020

{% tabs %}
{% tab title="New" %}
1. Unit 10-Status - Admin Customization
   * Communities can customize the default 10-06, 10-07, and 10-08 in status options for available, busy and unavailable. 
2. Affiliate Tracking System
   * A new affiliate system has been added to help Sonoran CAD grow and reward those who participate.
{% endtab %}

{% tab title="Changed" %}
1. PDF Records - Always Show
   * The action bar under police records will now always display the print to PDF option even if the user does not have permissions to modify or remove the record.
{% endtab %}
{% endtabs %}

### 1.9.4 \(Beta\) - 01/09/2020

{% tabs %}
{% tab title="New" %}
1. Record - Print to PDF
   * Police arrest, warrant, speeding and citation records can be printed as a PDF record.
2. Vehicle Citation - AKA
   * Added a civilian "AKA" field to the vehicle citation to stay consistent with other record types.
{% endtab %}

{% tab title="Changed" %}
1. Payments - Billing Address
   * Changed the wording for the billing address's "State" to "State/Province" and "ZIP" to "ZIP/Postal Code" to include non-American billing addresses.
{% endtab %}

{% tab title="Fixed" %}
1. General Citation - Supervisor Signature
   * Fixed an issue causing the supervisor signature on general citations to not save properly.
2. Arrest Record - Supervisor Signature
   * Fixed an issue causing the supervisor signature on arrest records to not save properly.
3. Vehicle Citation - Make
   * Fixed an issue where the vehicle make would not save properly in vehicle citation records.
{% endtab %}
{% endtabs %}

### 1.9.3 \(Beta\) - 01/08/2020

{% tabs %}
{% tab title="New" %}
1. Call Closed - 10-08
   * When a call is closed or a unit is removed, that unit is then marked as 10-08 \(Available\)
{% endtab %}

{% tab title="Fixed" %}
1. Modify Department
   * Fixed an issue causing users to be unable to modify an existing department.
2. Unverified Email
   * Fixed an issue causing users attempting to login with an unverified email address to receive a blank error message.
{% endtab %}
{% endtabs %}

### 1.9.1 \(Beta\) - 01/06/2020

{% tabs %}
{% tab title="New" %}
1. New Dispatch - 10-06
   * When receiving a new dispatch, units are automatically updated to 10-06 \(Busy\)
2. Voice Commands - Status
   * Voice commands for the unit status now include 10-97 and 10-23.
3. Account Subscriptions - Menu Access
   * The payment center to purchase and manage subscriptions is now also available by pressing the "Subscriptions" button at the community selections screen.
4. Payment Center - Discord Username
   * When starting a new subscription, the payment center now allows you to specify an optional discord username to add your "Customer" rank in our support discord.
5. Community Search - Autofocus
   * When searching for a new community, the community ID box is now auto focused when the popup modal is displayed.
{% endtab %}

{% tab title="Changed" %}
1. Dispatch - No Units
   * Dispatch Calls no longer require units to be attached. This allows dispatchers to create a queue of calls while awaiting available units.
2. Dispatch - Unit Attached
   * When a unit is newly attached to an existing call, their UI will alert them that this is a "New Dispatch" instead of an updated dispatch.
3. Penal Codes - Sort
   * Penal codes now sort by default based on the "Codes" column value.
4. Penal Code Charge - Sort
   * Penal codes in the dropdown search for records are now sorted in order by their "Code" value.
{% endtab %}

{% tab title="Fixed" %}
1. Voice Commands - 10 Status
   * Fixed an issue where the set unit status voice command would fail to register properly.
{% endtab %}
{% endtabs %}

### 1.9.0 \(Beta\) - 01/05/2020

{% tabs %}
{% tab title="New" %}
1. Payment Center
   * Sonoran CAD now has a built in payment center. Here, you can start, stop and manage paid subscriptions for your community. This is currently available in the admin panel’s limits section.
2. Unit Status
   * Units can now set their status to ENROUTE \(10-97\) or ON SCENE \(10-23\).
3. Dispatch - Call Status
   * Dispatch call statuses can now be set to either PENDING, ACTIVE or CLOSED and no longer contain status options that are unit specific.
{% endtab %}
{% endtabs %}

### 1.8.2 \(Beta\) - 01/02/2020

{% tabs %}
{% tab title="Changed" %}
1. Community Menu - Permissions
   * Community menu buttons are now only displayed if the user has the permissions, as opposed to simply being disabled if permissions are not present.
2. Bond Amount -&gt; Bond/Ticket
   * Changed the wording in the charges section from "Bond Amount" to "Bond/Ticket Amount"
{% endtab %}

{% tab title="Fixed" %}
1. Record - Add Button
   * Fixed an issue causing the "Add Record" button from not always displaying properly when generating a new police record on mobile devices.
2. Lookup Results
   * Fixed an issue where records would fail to display on the lookup results for mobile devices.
{% endtab %}
{% endtabs %}

### 1.8.1 \(Beta\) - 12/23/2019

{% tabs %}
{% tab title="New" %}
1. Lookup - Partial Search Terms
   * You can now input partial first names, last names, and plate numbers into a lookup search.
2. Voice Commands - Custom Trigger Word
   * Paid communities can now customize the voice command trigger word from "Sonoran" to a word of their choice.
3. Voice command improvements
   * Improved voice detection command computing and parsing. Sonoran CAD now dynamically computes where in your phrase the "plate" or "name" word starts and will string together the characters from there to search. Sonoran CAD also no longer looks for the "lookup" word in a hard-coded phrase index. This fixes issues where Google would detect "look up" as one or two different words. Sonoran CAD will also filter out words in-between the keyword and "plate" or "name."
4. Active Units - Status Dropdown
   * In the "Active Units" window, unit's 10-status now displays in a dropdown menu. This allows 10-statuses to be more easily updated without having to open the entire unit editor.
5. Dispatch Call - Block
   * Separate the dispatch call's street address into an optional block number and road.
6. DBSync Lookup - Get All Matches
   * Communities with DBSync now retrieve all characters matching the specified name instead of only the first result.
7. Warrant - Status Closed
   * If a warrant is served/closed, lookup results will not state "ACTIVE WARRANT" when running a lookup.
{% endtab %}

{% tab title="Fixed" %}
1. BOLO WebHook
   * Fixed an issue where BOLO notification webhooks went to the standard police record URL.
2. Get Vehicles - Name
   * Fixed an issue where searching for vehicle registrations to put on a record via name failed to return vehicles.
3. Call Closed - Clear
   * Fixed an issue where unit's screens would not be cleared fully when a dispatch call is closed.
{% endtab %}
{% endtabs %}

### 1.8.0 \(Beta\) - 12/22/2019

{% tabs %}
{% tab title="New" %}
1. Record Type - General Citation
   * Add a citation record type for all non-vehicle, arrest or warrant records. A written-warning type can also be toggled inside.
2. Window - Z-Indices
   * Clicking on a window will now bring it to the top layer.
3. Menu - Edit Account
   * Allow users to edit their account username, password and email preferences right from the community selection screen.
4. Record - Search for Vehicle
   * Added a search for existing vehicle registration feature for vehicle citations, arrests and BOLOs.
5. 11-Codes
   * 11-Codes can now be added in addition to standard 10-Codes.
6. UI - Color Improvements
   * Emergency pages now have a more standard grey-based color scheme for an overall better look and feel.
7. BOLO - Search for Civilian
   * Added a search for civilian feature on the BOLO creation window for a faster BOLO generation experience.
8. BOLO - Agency Location
   * When creating a new BOLO, agency location and ZIP code are now auto-filled for emergency units in a department with these values specified.
9. Arrest Record - Vehicle Year
   * Added vehicle year data to arrest record.
{% endtab %}

{% tab title="Changed" %}
1. Warrant - Header Wording
   * Changed "Warrant for Arrest" header title on warrant record to "Civilian Information" for a more encompassing and accurate section title.
2. Window - Handles
   * Changed the window handle positioning to be inside of the draggable window boundaries.
3. Arrest Record - Vehicle Section
   * Moved the arrest record's vehicle information section below the civilian section and above the arrest information section.
4. Modal Popup - Background Color
   * Changed the default dark purple gradient on popup modals to a dark grey gradient.
{% endtab %}

{% tab title="Fixed" %}
1. Dispatch - Online Units
   * Fixed an issue where dispatchers couldn't initially view all online units when first loading the page if they did not have fire, police or EMS permissions.
2. EMAIL - SMTP Timeout
   * Fixed an issue causing account creation emails to fail in rare cases due to an SMTP timeout.
3. Window - Page Boundaries
   * Fixed an issue where dragging windows to the edges of the page would cause scrollbars to appear due to an invisible overflow.
4. BOLO - Vehicle Year
   * Fixed an issue causing vehicle year values to not save in BOLO records.
{% endtab %}
{% endtabs %}

### 1.7.4 \(Beta\) - 12/20/2019

{% tabs %}
{% tab title="Changed" %}
1. Call Viewer - Typo
   * Fixed the "No Actice Calls" wording to "No Active Calls" in the dispatch call viewer.
{% endtab %}

{% tab title="Fixed" %}
1. Link Character
   * Fixed an issue preventing users with database sync from linking a new character.
2. Dispatch - No Postal
   * Fixed an issue causing dispatches without a postal code to fail.
{% endtab %}
{% endtabs %}

### 1.7.3 \(Beta\) - 12/19/2019

{% tabs %}
{% tab title="New" %}
1. Transfer CAD Ownership
   * Community owners can now transfer ownership of the CAD in the admin menu. This requires email verification.
2. Account Status - Permission Keys
   * Permission keys now update the user account status from "PENDING" to "ACTIVE" as long as the user account has not been banned.
{% endtab %}

{% tab title="Fixed" %}
1. Permission Keys
   * Fixed an issues causing permission keys to not be successfully updated with in-depth permissions.
2. Save Permission Key
   * Fixed an unhandled exception when saving permission keys in specific cases.
3. Admin Accounts Permission
   * Fixed an issue where permission keys with the admin "Accounts" permission would not properly have this permission applied to the user.
{% endtab %}
{% endtabs %}

### 1.7.2 \(Beta\) - 12/18/2019

{% tabs %}
{% tab title="Changed" %}
1. Menu - Update Permissions
   * Forced users to retrieve new local permissions for client-side checks whenever they access the community menu page.
{% endtab %}

{% tab title="Fixed" %}
1. Admin In-Depth Permissions
   * Fixed an issue preventing user's updated in-depth permissions from displaying properly in the admin account menu.
2. Admin - Status Permissions Change
   * Fixed an issue causing user in-depth permissions to not all be disabled when an account status is changed to PENDING or BANNED.
{% endtab %}
{% endtabs %}

### 1.7.1 \(Beta\) - 12/18/2019

{% tabs %}
{% tab title="Changed" %}
1. Community Limits - Security
   * Fixed an issue causing the community API key to be exposed in websocket data transfers for admins that do not have the in-depth limit permissions.
2. Community Accounts - Security
   * Fixed a security vulnerability allowing admins without account editing permissions to still retrieve community account information.
{% endtab %}

{% tab title="Fixed" %}
1. Account Permissions
   * Fixed an issue where editing a user's account permissions in the admin menu incorrectly updates the admin's permissions instead of the selected account.
2. Admin - Loading
   * Fixed an issue causing the admin page to continually load if the admin does not have user account editing permissions.
{% endtab %}
{% endtabs %}

### 1.7.0 \(Beta\) - 12/18/2019

{% tabs %}
{% tab title="New" %}
1. In-Depth Permissions
   * A more in-depth permissions system allows admins to specify more in-depth permissions.
2. Live Map
   * Paid communities can specify a link to a map \(commonly used as a live map\) for their community. This can be viewed in a pop-out window for all emergency units and dispatchers.
3. Police - Edit Other Units
   * Emergency units with permissions can select a unit in the "Active Units" window to edit their rank, status, department, etc.
4. Discord Configuration - Menu
   * Communities can now specify their community Discord invite link to be displayed in the community menu.
5. Website Configuration - Menu
   * Communities can now specify their community website link to be displayed in the community menu.
{% endtab %}

{% tab title="Changed" %}
1. Permission Keys - Admin UI
   * Improved the layout of the permission key configuration panel in the admin UI for mobile screens.
2. Emergency Pages - Top Action Bar Widths
   * Increased the container widths for all emergency pages. This allows all action buttons to display on one line for medium sized screens.
3. Menu - Permission Key UI
   * Improved the UI layout of the permission key input and button on the community menu page.
{% endtab %}

{% tab title="Fixed" %}
1. Account Permissions
   * Fixed an issue where editing a user's account permissions in the admin menu incorrectly updates the admin's permissions instead of the selected account.
2. WebHooks
   * Fixed a bug causing police record Discord webhooks to fail with empty fields.
{% endtab %}
{% endtabs %}

### 1.6.0 \(Beta\) - 12/15/2019

{% tabs %}
{% tab title="New" %}
1. Permission Keys
   * Allows admins to generate permission keys for users to enter at the community menu. These keys will grant the users the specified permissions.
2. Discord WebHooks
   * Discord webhook integration can be specified in the admin panel. Discord webhooks can be sent for new dispatches, records, BOLOs, etc.
3. Create Record - Autofill Civilian
   * When filling out a record, officers can search for a registered/created civilian to auto-fill their information.
4. Department - Configure Location
   * Admins can specify department location and zip code to auto-fill when creating a new record.
5. Penal Code - Jail Time
   * Added a jail time specification box in the penal code specification section. 
6. Penal Code - No Bail
   * Added a “No Bail” option on the penal code’s bail type drop down.
7. Civilians - Auto Approve DMV Records
   * Civilians with DMV permissions can now modify and approve their licenses and vehicle registrations directly from the civilian page.
8. Login Page - Email Auto Focus
   * Login page email field now is auto-focused for a faster sign-in.
9. Lookup - Auto Focus
   * Opening a new lookup tab will auto-focus the first name box in the search bar for faster searching.
10. Record Viewer - Height Optimizations
    * Improved dynamic height calculations for record viewing component.
11. DBSync - Empty Table Check
    * DbSync now checks for an empty table case when testing mappings.
{% endtab %}

{% tab title="Fixed" %}
1. Penal Code - Infraction and Warning
   * Fixed an issue where editing a penal code to type "Infraction" or "Warning" would cause the penal codes to fail to display.
2. Full Screen Scrolling
   * Fixed an issue that prevented users from scrolling in the in-game integration section and other extended sections while in full screen mode.
3. Penal Code Types - Warning and Infraction
   * Fixed an issue where the new penal code types "WARNING" and "INFRACTION" were not properly displaying in the admin editor.
4. Call Description Scrolling
   * Fixed an issue where a call description is not scroll-able for units on a call.
5. Civilian - Eye Color
   * Fixed an issue where when creating a new character the eye color drop-down would fail.
6. User Accounts - Autofill
   * Prevented Chrome's autocomplete from filling out the admin accounts section search box with the user's saved username.
7. Kick Unit - Permissions
   * Fixed an issue where only admins could force kick units instead of dispatchers.
8. Registration - Email Spaces
   * Prevented users from registering an account with a space in the email address.
{% endtab %}
{% endtabs %}

### 1.5.4 \(Beta\) - 12/03/2019

{% tabs %}
{% tab title="New" %}
1. Voice Commands - 10-Status
   * Units can now set their 10-Code status via voice command. "Sonoran, set status "
2. Dispatch - Toggle Unit Panic
   * Dispatch can select a unit and manually toggle their PANIC state on or off.
3. Dispatch Kick Unit
   * Dispatchers can now select a unit to forcefully kick them back to the community menu. This is useful for AFK units that have not disconnected/closed the CAD or have not navigated away from the police, fire or EMS page.
4. Character Age - Computed from DOB
   * Civilian Character age will be calculated from their DOB.
5. DMV - Remove Record
   * Removing a license or vehicle registration in the DMV page now automatically removes it from the UI without having to refresh the search.
{% endtab %}

{% tab title="Changed" %}
1. Dispatch Updated - Shorten Notice
   * When a dispatch call is updated, text-to-speech simply states, "Dispatch Updated." This will shorten the lengthy text-to-speech response whenever a call is modified.
2. Primary Officer -&gt; Primary Unit
   * Changed the wording of "Primary Officer" on a dispatch call to "Primary Unit" - This helps better encompass the phrasing for a fire or EMS dispatch.
3. Mobile - Admin Codes UI
   * Improved the UI positioning for admin penal and 10-code editing for mobile devices.
4. Mobile - Window Vertical Position
   * Raised the new window vertical position for an improved mobile UI experience.
{% endtab %}

{% tab title="Fixed" %}
1. Unit Disconnect
   * Fixed an issue where units would only be removed from the dispatch viewer if the app or window was closed. Sonoran CAD now properly removes the unit upon page navigation away from police, fire or EMS.
2. DMV - Submit Vehicle Registration
   * Fixed an issue where DMV submitting a new vehicle registration would fail.
3. Penal Code Types - Warning and Infraction
   * Fixed an issue where the new penal code types "WARNING" and "INFRACTION" were not properly displaying in the admin editor.
4. DB Sync Characters
   * Fixed an issue where an account's linked characters would fail to load when using database sync.
5. Login Button - 404
   * Fixed an issue where the "login" menu button would take you to a 404 page on certain pages.
6. Record Editor - Border Height
   * Fixed an issue where the record editor save and remove button container was displayed slightly outside the window border.
{% endtab %}
{% endtabs %}

### 1.5.3 \(Beta\) - 11/30/2019

{% tabs %}
{% tab title="New" %}
Delete/Remove CAD

* Community owners can now remove their CAD system in the admin menu. This process requires email verification.

1. Penal Code Types
   * Added "Infraction" and "Warning" to penal code charge type options.
2. Record Charges - Mobile Optimization
   * Improved UI layout for police record charges.
3. Lookup Results - Mobile UI Optimization
   * Increased record lookup results height for mobile users.
{% endtab %}

{% tab title="Fixed" %}
1. DMV Record - Mobile Height
   * Fixed an issue where DMV records on mobile wouldn't be tall enough to scroll.
2. DMV - Mobile Height
   * Fixed an issue where the "New Record" section on mobile took up the entire screen.
3. DMV Pending and Search
   * Fixed an issue where dynamic SQL queries were not formatted correctly when searching for DMV records.
4. Community Characters Table
   * Fixed an issue where community character tables were not properly generated upon CAD registration.
5. Validation Redirect
   * Fixed an issue preventing the validation page from properly redirecting the user to the login page.
{% endtab %}
{% endtabs %}

### 1.5.2 \(Beta\) - 11/29/2019

{% tabs %}
{% tab title="New" %}
1. Primary Unit - Search Filter
   * The "Primary Unit" box on the call editor is now a search/filter for units only currently attached on the call.
2. Login - Prevent Spaces
   * Sonoran CAD now prevents a user from accidentally entering a space in their user account login.
{% endtab %}

{% tab title="Changed" %}
1. Unit Info - Display Department
   * Changed the unit information at the top of the page to show the department name instead of the subdivision name.
{% endtab %}

{% tab title="Fixed" %}
1. DMV Loading Failure
   * Fixed an issue preventing the DMV page from loading properly.
2. DB Sync Disable Toggle
   * Fixed a bug causing disabled toggles for the Database Sync configuration to still be toggleable.
3. Lookup Voice Commands - Bug
   * Fixed an issue causing voice command name and plate searches to not work properly.
{% endtab %}
{% endtabs %}

### 1.5.1 \(Beta\) - 11/28/2019

{% tabs %}
{% tab title="New" %}
1. Connection Event Handler - Redesign
   * A new connection and websocket event handling system to improve performance and fix common bugs involving connection registration failures. This improves overall application stability and reliability.
{% endtab %}

{% tab title="Changed" %}
1. Community Cards - Display Bug
   * Certain screen sizes do not show community cards on the menu page.
2. Department Structure - Admin
   * Fixed an issue where the editing department structure in the admin panel failed to load.
3. NULL DB Sync Structure
   * Fixed a bug where new communities would have a NULL DB Sync structure. This would throw an error when accessing the civilian page.
4. Lookup - Empty After Navigation
   * Fixed a bug where after navigating away from the police or dispatch page, the records would not display.
{% endtab %}
{% endtabs %}

### 1.5.0 \(Beta\) - 11/27/2019

{% tabs %}
{% tab title="New" %}
1. Database Sync
   * Communities can specify a SQL connection string and mapping for their database structure for characters, vehicle registrations and licenses.

     Sonoran CAD will then search for characters, vehicle registrations and licenses directly from your community's database for full integration!
2. Subscription Upgrades
   * A payment system for communities to upgrade their limits, enable new features and more!
3. Civilian Page
   * A page for civilians to create a character, make emergency calls, view licenses, view vehicle registrations and more.
4. DMV Page
   * A page to edit, add and remove vehicle licenses and registrations for civilian characters.
5. Licenses
   * Civilian license records can be created, modified and searched.
6. Vehicle Registrations
   * Civilian vehicle registration records can be created, modified and searched.
7. BOLO System
   * A way for police and dispatch to add, edit, search, and remove BOLOs.

     BOLOs can be viewed in the BOLO window or in an applicable name/plate search.
8. License Type Customization
   * Communities with this feature can customize their civilian license types.
9. Community Info Customization
   * Your community ID, name, subtitle and image can now be changed in the customization menu in the admin panel.
10. Community Limits Panel
    * View your community CAD limits in the "Limits" section in the admin panel.
11. Lookup - Dynamic Tabs

    * The lookup window now only displays record tab types \(BOLO, Warrant, Arrest, etc.\) if they are present.

      When no results are found, a "No Records Found" message is displayed.

    12. Record Tabs - Dynamic

    * When running a lookup, the selected record tab will now be set to the first record type available based on priority.

    13. Unit Info - Clear Department

    * Add the ability to quickly clear a unit's agency, department or subdivision in the unit editor.

    14. PWA Auto Updater

    * You will no longer have to clear your local cache to get the latest Sonoran CAD version.
{% endtab %}

{% tab title="Changed" %}
1. District Rename to Agency
   * "Districts" are now called "Agencies" - The full structure is as follows:

     Agency &gt; Department &gt; Subdivision
{% endtab %}

{% tab title="Fixed" %}
1. Socket Connection Event Registering
   * Added additional functionality to more properly handle server-client web socket event registering, destruction and re-registering.
2. Lookup Voice Command - Plate Tab
   * Fixed an issue where looking up a vehicle plate via voice command has the lookup name tab still shown.
3. Page Reseize
   * Fixed an issue where rotating a mobile device or resizing the page would limit the view-able area when switching back,
4. Unit Info - Updated
   * Fixed a bug where updating a unit's information does not display until after a page refresh.
5. Downloads/Discord - Connection Error
   * Fixed an issue causing the downloads and discord pages to have a server connection error on a fresh page load without user navigation.
{% endtab %}
{% endtabs %}

### 1.4.0 \(Alpha\) - 11/15/2019

{% tabs %}
{% tab title="New" %}
1. Penal Codes
   * Penal codes can now be added, edited and removed in the admin menu. 
2. Records Charges - Penal Code Select
   * Police/Dispatch can now add charges by filtering for a specific penal code.
3. Penal Code Window - Police/Dispatch
   * A new window for police to view and search for penal codes.
4. Voice Commands - Lookup
   * The ability to lookup a name or license plate via voice commands. “Sonoran lookup &lt;name/plate&gt; &lt;plate/name&gt;”
5. Record Notice Flags
   * Special flags can be added to a name or license plate to be shown when running a lookup. \(Armed, Mentally Ill, etc.\) These flags are also be repeated aloud by TTS to help officers running lookups via voice commands.
6. Improved Dynamic Window Height
   * Dynamically computed popup window height based upon number of results and content within a window.
7. 10-Codes Filter Search
   * Allows dispatchers to search for a 10-Code in the call editor drop down. This enables faster call creation for communities with a large quantity of 10-Codes.
8. Fire Page
   * Page for users with the FIRE permission to receive dispatch calls.
9. Ems Page
   * Page for users with the EMS permission to receive dispatch calls.
{% endtab %}

{% tab title="Changed" %}
1. Community Selection - Height
   * Community cards in horizontal scroll are now sized more dynamically, greatly improving user's mobile experience.
2. UI Improvements - Color
   * New colors, layouts, borders, etc.
{% endtab %}

{% tab title="Fixed" %}
1. 10-Codes Duplication
   * Fixed an issue where adding a new 10-Code, causes the new code to be duplicated until the codes have been refreshed.
2. Re-Connection Bug
   * Fixed an issue when the application re-connects to the Sonoran API server, events are not re-registered properly to the new connection. This can cause issues preventing a user from logging in or making any actions particularly on mobile platforms.
3. Text-To-Speech Voice
   * Sonoran CAD now searches for the "Google US English" speech synthesis option. Otherwise, use the default system voice. Fixes consistency issues across systems.
4. Voice Commands - Page Navigation
   * Fixed issue causing voice commands to fail after navigating away and back from an emergency page.
{% endtab %}
{% endtabs %}

### 1.3.2 \(Alpha\) - 11/09/2019

{% tabs %}
{% tab title="New" %}
1. PWA App Installations for OSX and iOS
   * PWA \(Progressive Web Application\) installations have been configured for all platforms, but specifically allows OSX and iOS users to experience a native app experience with Sonoran CAD. For more information, view the \#downloads channel in Discord, or click “Downloads” on the side navigation menu on the website.
{% endtab %}

{% tab title="Changed" %}
Desktop - Splash Screen Font

1. * Updated the splash screen font for the electron desktop application for windows
{% endtab %}

{% tab title="Fixed" %}
1. 10-Codes - Admin
   * Fixed an issue causing 10-Codes to not appear for editing on the admin panel.
{% endtab %}
{% endtabs %}

### 1.3.1 \(Alpha\) - 11/06/2019

{% tabs %}
{% tab title="New" %}
1. Desktop - Splash Screen
   * A new splash screen has been added to the Sonoran CAD Windows desktop application. This smooths out the loading and update checking process.
2. Vehicle Citation - Court Time
   * The court time for the court date has been added onto the vehicle citation record type.
{% endtab %}

{% tab title="Changed" %}
1. Vehicle Citation - Date Validation
   * Default date values have been added for the vehicle citation court date and license expiration. This removed the defaulted red warnings.
{% endtab %}

{% tab title="Fixed" %}
1. Page Scroll - Bug
   * Fixed an issue disabling vertical scrolling on smaller pages.
2. Call Viewer - Medium Display
   * Fixed an issue causing inputs on the call editor/viewer to be uneven on medium sized screens.
3. 10-Codes - Empty Dropdown
   * Fixed an issue causing the 10-codes drop down to be empty for the dispatch call editor.
4. New Record Number - Dispatch
   * Fixed an issue causing the new record number to display as -1 for dispatchers.
{% endtab %}
{% endtabs %}

### 1.3.0 \(Alpha\) - 11/05/2019

{% tabs %}
{% tab title="New" %}
1. Warrants
   * Police and dispatch can now add, edit, search and remove arrest warrants.
2. Vehicle Citations
   * Police and dispatch can now add, edit, search and remove vehicle citations.
3. View Online Units
   * Police can now press the “Online Units” button to view all active units on their CAD server.
4. View 10-Codes
   * Police and dispatch can now press “10-Codes” at the top menu to view all custom 10-codes currently configured.
5. Stay Signed In
   * Select “Stay Signed In” on the login page to reduce the amount of times a sign in is required.
6. Lookup Search - Shortcut
   * Police and dispatch can now press enter/return in the lookup textbox to search faster than manually pressing the search button.
7. Police Call Viewer - Status
   * Added new functionality to update units on the police call viewer in real time \(status changes\).
8. Support Discord Links
   * Navigation links to the Sonoran CAD Discord have been added to the side navigation menu.
9. Reset Password - Email Template
   * Added a new styled password reset email template for Sonoran CAD password reset functionality.
10. UI Improvements
    * General UI improvements, darker theme, window calculation sizes, button colors and more!
{% endtab %}

{% tab title="Fixed" %}
App Logo - Android

1. * Fixed an issue causing the splash screen logo on Android to get cut off.
{% endtab %}
{% endtabs %}

### 1.2.1 \(Alpha\) - 10/30/2019

{% tabs %}
{% tab title="New" %}
1. Mobile Action Menu
   * Police and Dispatch pages now have a dropdown "Actions" menu for all action buttons
{% endtab %}

{% tab title="Fixed" %}
1. Desktop Download Link
   * Fixed an issue causing the Windows download link at homepage to be outdated.
{% endtab %}
{% endtabs %}

### 1.2.0 \(Alpha\) - 10/29/2019

{% tabs %}
{% tab title="New" %}
1. Sonoran CAD Windows Desktop Application
   * Downloadable desktop application for OSX and Windows, powered by Electron. Download link displays for desktop browser users.
   * NOTE: During the Alpha release, the Windows EXE is not currently signed with a developer certificate. You may see warnings on install.
2. Custom Window and Tab System
   * A fully custom draggable, resizable window and tab system. You can minimize, open, close, etc.
   * This allows users to open multiple record or lookup windows at one time, improving multi-tasking.
   * NOTE: The MAXIMIZE functionality has not yet been added.
3. Arrest Records
   * Arrest records can now be added, edited, searched and removed.
   * Create a new arrest record by pressing the "New Record" button on the police or dispatch page.
   * NOTE: Other record types will be added shortly, this is just to test the functionality of the system.
4. Records Lookup
   * Police and dispatch users can now press the "Lookup" button to open a new records search window.
   * Users can enter a full or partial name, or search by a license plate.
   * NOTE: Currently, only arrest records are shown, more will be added soon.
5. Voice Commands - PANIC
   * The police page will now prompt users for access to their microphone \(Chrome\).
   * The voice command "Sonoran Panic" will toggle your unit's PANIC state.
{% endtab %}

{% tab title="Changed" %}
1. Session Storage
   * Cookies are no longer used to store user's session IDs and information required to handle a page refresh.
   * Local browser session storage is used in place of prior cookie storage.
2. No-Reply Registration Email
   * Sonoran CAD now sends all emails from no-reply@sonoransoftware.com
3. Dispatch - Separate Connection Grouping
   * Dispatchers are now added to an additional SignalR grouping.
   * This will be to ensure server calls \(Ex: ackDispatchCall\) are only sent to dispatchers, and not all other units within the server.
4. Dispatch - Postal or Address
   * Dispatches now only require the postal or address.
   * Text-to-speech notifications state the postal and/or the address when applicable.
5. Department Structure - Table Wording
   * Admin department structuring, changed to "Districts/Departments/Subdivisions" per page for the table view amount.
{% endtab %}

{% tab title="Fixed" %}
1. Reset Password
   * Fixed an issue with the reset password system not working properly.
   * NOTE: These UI elements are outdated and will be modified soon.
2. Toolbar - Mobile
   * Fixed an issue causing the top toolbar "Sonoran CAD" title gets cut off and brought down on mobile screens.
3. Department Structuring - Toggle Edit
   * When modifying a community's department structure, the background now properly turns red to inform the user that the editing mode is toggled.
4. Registration Email Template
   * Fixed the background of the Sonoran LLC logo.
5. Disconnection - Null Value
   * Disconnection context values being NULL after hours of inactivity.

     Fixed an issue where this causes an unhandled exception after disconnection from the connection hub.
{% endtab %}
{% endtabs %}

### 1.1.0 \(Alpha\) - 10/15/2019

{% tabs %}
{% tab title="New" %}
1. Police Panic Button
   * Police units can press the red "PANIC" button to inform other online units and dispatchers when in distress. This will pulse the screen red for the unit. The unit on the dispatcher panel will also pulse red.
2. Audio Alerts
   * Police unit's will recieve customized audio alerts when a dispatch is created, updated or removed.
   * Police unit's will hear a brief tone when changing their 10-status. \(10-06, 10-07, 10-08\)
3. Settings Modal
   * The left drawer now contains a "Settings" option. Opening this will allow the user to change their system volume for audio alerts and tones.
4. Dispatch Call - Unit Removal Logic
   * Sonoran CAD now tracks the removed units when updating a call. Removing units from a call will now inform the unit that the call is closed \(for them\) and will clear their screen.
5. Dispatch Active Calls - 10-Status Logic
   * Unit 10-Statuses are updated in real-time. However, when a new dispatcher first loads in, existing calls are pulled from the database. When a unit updates their status, this is not updated in the unit's current active call. As a result, dispatchers loading in previous calls will show unit's status colors incorrectly. Dispatchers now search locally for updated unit statuses on their active calls list.
6. Status - Cooldown
   * A 500ms cooldown delay has been added to prevent units from spam updating their status.
{% endtab %}

{% tab title="Changed" %}
1. Title Bar and Icon
   * The top title bar and icon of the website now displays "Sonoran CAD" and the Sonoran Logo.
2. Login Logo Padding
   * Additional margin space added to the top of the Sonoran logo on the login page for mobile users.
3. Popup Modal Color
   * Popup editor modal backgrounds have been changed from a red-blue gradient to a dark purple gradient.
4. Side Drawer
   * The side navigation drawer is now NOT displayed by default. The drawer now lays over the screen and does not push content over.
{% endtab %}

{% tab title="Fixed" %}
1. Unit Overflow - Mobile
   * Call editor with multiple units can no longer flow over and cover up the call editor.
2. Duplicated Server Calls
   * Fixed issue with client websocket events not being properly un-registered when navigating away from a page.
3. Switch Community
   * Fixed a bug causing users to be unable to view navigation buttons when switching communities without a page refresh.
4. Community Menu
   * Fixed an issue causing the community menu to be blank when navigating back after a page refresh.
5. Police - Empty Call
   * Fixed an issue causing an empty/no active call from displaying some information on the police call viewer. These fields are now blank instead of displaying default values.
6. Sidebar Navigation Items
   * Fixed an issue where sidebar navigation items would be incorrect when refreshing the community admin, police or dispatch page.
{% endtab %}
{% endtabs %}
