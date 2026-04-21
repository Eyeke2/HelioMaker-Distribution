Version 1.6.0

* Added License Management PIN protection for HelioMaker license activations, providing an extra security layer beyond the license key and email address
* Updated the License Activations Manager user interface with dedicated Activate and Deactivate buttons and improved activation status presentation for the current machine
* Improved overall user interface responsiveness
* Menu item descriptions now display correctly in the bottom status line while navigating the Setup and Help menus
* Added an Exit command to the Setup menu and improved protection against inadvertent program closure
* Added `F1` and context help shortcuts to the Dynamic Tracking and Find & Track dialogs
* Bug fixes and stability improvements

* Special notice for all users: Support for the legacy license activation management interface used by older HelioMaker versions is scheduled to end on August 1, 2026.
  After this date, older versions of HelioMaker may no longer be able to retrieve and manage existing license activations. This change does not affect the validity of your
  existing license activations themselves - it only affects the legacy activation management function in older versions. To continue using License Activations Manager,
  please update to version 1.6.0 or later and set up a License Management PIN.
* The license terms and EULA statements have also been updated in this release, so please read them carefully.
  Installing this update constitutes agreement to the applicable license terms.

Version 1.5.0

* Added Dynamic Target Tracking for real-time tracking rate updates of the Sun, Moon, and major solar system bodies
* Improved lunar and solar guiding, daytime polar alignment and PHD2 calibration workflows when using Dynamic Target Tracking
* Added delayed sequence start for better session scheduling
* Added an Advanced Setup option to define each capture cycle by time limit in seconds instead of frame count
* Improved tracking rate status indication and updated the built-in help documentation, including revised workflow recommendations

Version 1.4.4

* Fixed Lucky Imaging (Live Stack) mode
* Bug fixes and stability improvements
* Updated the bundled Microsoft Visual C++ Redistributable to version 14.50.35719.0
* Enhanced license security and updated server infrastructure
* Improved update reliability in some cases where antivirus software could interfere with automatic updates.
Also enhanced the visual appearance of the upgrade process with a new background image

Version 1.4.2

* Fixed default capture folder path
* Create capture folder if it doesn't exist
* Added ST-4 guiding support with Virtual Planetary Camera (experimental, requires PHD2 v2.6.13dev8-solar.2)
* Resolved an issue where SharpCap overlays appeared in frames delivered to HelioMaker;
HM now receives calibrated images only. Requires SharpCap v4.1.13651.0 or later.
* Updated bundled Microsoft Visual C++ Redistributable to 14.50.35710.0

Version 1.4.1

* Fixed an issue that could deactivate license during a cloud infrastructure disruption
* Bug fixes and stability improvements

Version 1.4.0

* Extended code signing certificate validity by three years
* Set the default installation folder to "Program Files" instead of the legacy "Program Files (x86)" path
* Bug fixes and stability improvements

Version 1.3.9

* Automatically update the PHD2 lock position to the center of the detected object when detection settings change in Find \& Track (Full Disk/Crescent and Planetary modes)
* Recommend updating PHD2 to v2.6.13dev7-solar.rc5

Version 1.3.7

* Updated and corrected PHD2 calibration help

Version 1.3.6

* Added display of remaining free disk space
* Added display of completed cycles during a sequence
* Increased timeout for retrieving the list of PHD2 profiles
* Added an error message if no mount is selected in the PHD2 profile
* Updated help documentation for daytime polar alignment

Version 1.3.5

* Added support for MONO12 camera format
* Bundled Microsoft Visual C++ Redistributable v14.44.35211.0
* Bug fixes and stability improvements

Version 1.3.3

* Updated help documentation for daytime polar alignment
* Bug fixes and stability improvements

Version 1.3.1

* Improved handling of guiding pauses in PHD2 (requires PHD2 v2.6.13dev7-solar.3 or later)

Version 1.3.0

* Improved reliability of surface feature tracking
* Added surface tracking configuration option in Advanced Settings for finer control
* Refined guiding lock position handling in the user interface
* Minor bug fixes and stability improvements

Version 1.2.5

* Maintenance release addressing launch failure if the required Microsoft Visual C++ Redistributable is missing

Version 1.2.4

* Changed architecture to 64-bit
* Added automatic version update checking
* Added Find \& Track tool
* Added support for guided lucky imaging
* Improved stability
* Refined user interface with updated graphics and better support for High-DPI displays

Version 1.0.8

* Added Microsoft 2015-2022 Redistributable x86 Runtime (14.42.34433.0) as part of installer
