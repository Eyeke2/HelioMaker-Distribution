Version 2.0.7

* Atmospheric refraction is now a single **Apply standard atmospheric refraction** setting in Plan preferences, replacing the temperature and pressure controls that were in the pre-flight. Refraction shifts the contact times, so the setting is saved with the plan and is on by default; changing it re-solves the contacts and refits every phase to its new window. The pre-flight shows the current choice as a readout
* The solar filter density list now offers **ND 5.3, 5.6 and 5.9** for a certified solar filter with extra neutral density stacked behind it, one, two and three stops denser than ND 5.0 film. Select the total density of the stack when your rig still overexposes the disk at its shortest usable exposure, instead of shortening the exposure below about a millisecond and paying for it in noise
* The eclipse pre-flight checklist can now be hidden from its summary banner, so the arm and cancel buttons stay within reach on a short screen. The go/no-go verdict stays visible while the checks are collapsed
* Eclipse capture is considerably more resilient around the critical phases, recovering from lost capture commands and from the live view and still image switches either side of totality, so a single dropped instruction no longer costs a phase
* Fixed **Finish, then switch** at a phase boundary while capturing in live view. A recording that was still completing at the boundary could be cancelled as though it had overrun, leaving its frames set aside for review instead of being saved normally
* Fixed a rounding error in the phase timing after the eclipse
* Fixed license, clock and update notices going quiet for the rest of the session after an update was agreed to and the exit was then cancelled, for example because an eclipse run was in progress
* Fixed notices being lost when the startup splash screen was dismissed with a click rather than left to close on its own
* The startup splash screen now stays up for its first three seconds instead of vanishing on a stray click or keypress, so a window opening behind it is no longer dismissed by accident
* Fixed the guiding camera name in Plan preferences keeping the previous value after switching between a physical guiding camera and a shared camera
* The warning about a phase overrunning into the next one now measures live view correctly. A run of equal short exposures is recorded as a single file and finishes as a whole, which the estimate previously counted as one frame
* Updates and unrequested pop-ups are now blocked outright from 12 hours before your eclipse until 12 hours after it. Nothing can restart HelioMaker or change the system clock across eclipse day, and a notice that would have arrived in that window waits until it has passed. The tools you open yourself, including the pre-flight clock check, are unaffected
* Installing an update no longer asks you to confirm the exit a second time, nor about mount tracking rates. Confirming the update is taken as your answer, and the mount keeps the tracking rate it is already running
* The update installer now starts only once HelioMaker has fully closed, rather than alongside the shutdown, so it can no longer begin replacing files while the application is still using them
* Updates are no longer offered while a sequence, an eclipse run, a scan or the eclipse pre-flight is in progress, so a capture cannot be interrupted by an update notice. A notice that arrives at a busy moment now waits for a quiet one instead of opening on top of another window
* The Clock sync tool now says when the system clock is too far out for it to correct, instead of requesting administrator rights and then failing. It corrects drift of up to a day; a larger difference is set in Windows time settings
* Guiding and focus now read the same way in both eclipse console sizes. Each occupies a full-width bar with its own icon, and both stay on screen for the whole run rather than one disappearing when nothing is scheduled
* A mount that is parked, stopped or slewing is now reported in red as the leading fact on the guiding bar, for example **Mount parked, waiting for unpark**. Guiding cannot run at all until the mount tracks again, so the console no longer leads with what the plan asked for and buries the reason nothing can guide
* Notices that arrive on their own now wait for a quiet moment instead of opening on top of a window you already have open. This covers the mount altitude safety stop, the cached ephemeris warning, PHD2 calibration results and scan completion. Where the fact is already on screen, as with a failed slew, the status line carries it rather than a pop-up. The safety stop itself is never delayed, only its explanation
* Fixed the **Overrun** setting in the phase editor cutting its longer choice short
* HelioMaker now closes reliably while a background lookup is still running. Time zone, clock verification and comet magnitude lookups against a slow or unreachable network no longer delay or block shutdown
* Corrected eclipse run summaries and timing reports. A run that captured nothing, stopped early, lost timing records or ended with a failed capture phase can no longer be presented as a successful run with perfect timing; phases already past when the run was armed remain neutral context rather than false failures

Version 2.0.6

* Added a **timeline preview** to the Solar Eclipse Planner. Play the selected eclipse and watch the simulated view, cursor readout and contact markers sweep the whole timeline, slowing automatically around second and third contact so the diamond ring, Baily's beads and totality are easy to follow
* The enlarged simulation view now stays open while the preview plays, so the entire eclipse can be watched at the larger size
* Smoother and sharper eclipse simulation. The Sun and Moon now move fluidly instead of stepping, limb edges are cleaner, and Baily's beads render as tighter, more distinct points
* The simulation now sets behind a horizon. For an eclipse whose contacts fall below the horizon, the Sun and Moon sink out of sight at zero altitude and the sky goes to twilight, instead of the view continuing to show an eclipse that cannot be seen from your site
* Fixed the mouse-wheel controls in **Find & Track**. On some systems they did nothing at all, depending on the Windows "scroll inactive windows" mouse setting. Resizing the search zone and adjusting the size lock now respond wherever the pointer is. The crescent detection actions are also mutually exclusive now, so the intended one is always the one applied
* Fixed button and icon scaling in the Solar Eclipse Planner on high-DPI displays. The lock, undo and timeline preview buttons no longer appear oversized, and their artwork is sharp and sits correctly inside the button
* Clearer guidance when opening the Ephemeris Planner or Solar Eclipse Planner without an observer location, explaining how the site is read from the mount

Version 2.0.5

* Added the new **Solar Eclipse Planner and Imaging Tool**, the centerpiece of HelioMaker 2.0. It provides site-specific eclipse planning, detailed contact and phase timing, draft and final imaging plans, simulation and rehearsal, comprehensive pre-flight checks, and automated SharpCap capture through the partial phases, thin crescents, diamond rings and totality
* Eclipse imaging includes coordinated camera-mode and exposure changes, PHD2 guiding and recovery, planned refocusing, solar-filter and spoken cues, live phase and capture telemetry, shutter-sound feedback, storage protection, and safeguards for resuming or restarting a session
* Added the new **Ephemeris Planner** for finding and preparing observing windows using JPL Horizons and locally cached ephemeris data, with altitude plots, observer-local time handling, lunar phase and magnitude information, target history, and safety-checked mount slewing
* Extended Dynamic Target Tracking and guiding to comets, asteroids, minor solar-system bodies and natural satellites, including support for custom mount rates and PHD2 lock-position shifting where appropriate
* Added the **SHG Scanner** for automated solar spectroheliograph scans in right ascension or declination, with SharpCap capture control, guiding coordination, mount-return handling and movement safety checks
* Added automatic SharpCap refocusing, sequence pause and resume coordination, and guiding recovery after refocusing or other planned interruptions
* Significantly improved Full Disk/Crescent and Surface detection, reacquisition and stability reporting. HelioMaker detection is now available consistently with supported physical PHD2 guide cameras as well as shared-camera configurations
* Added a focal-length calculator and a focal-length estimator based on measured Sun or Moon size, together with new UTC time-checking and synchronization tools
* Modernized dialogs, status indicators, collapsible panels, artwork and high-DPI presentation, while reducing user-interface flicker and improving responsiveness
* Improved license renewal and activation management, encrypted locally stored license data, expanded expiry reporting, and refined license-management dialogs
* Numerous improvements to stability, detection algorithms, mount and PHD2 control, SharpCap communication, shutdown handling, error recovery and diagnostic reporting

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
