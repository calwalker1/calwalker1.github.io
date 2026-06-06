# Hopper — Release Notes

============
# Version 0.54
XX April 2026

#Show Management#
- FIXED: Deleting the first video in a multi-video performance no longer causes the second video to disappear and the first video's label to be cleared. The remaining video is now correctly promoted to primary.

#Console connection#
- FIXED: Selecting MA3 now opens the UDP connection 

#Analysis#
- Better OCR (text reading) skills in hopper to prevent slashes (/) being detected as 1. Additionally logic now applies so if the OCR does detect a 1, Hopper will see that this is likely an errror for instance detecting cue 1,2,3,13,4,5 likely means the 13 is actually /3 and disregards.
- Hopper can now handle centre-justified text and auto expands left and right instead of just right.



============
# Version 0.53
26 April 2026

#General#
- Hopper will now ask for permission to collect system information after your second launch and send these to Calibrated Productions databases hosted on Cloudflare. You can change your response any time via the user preferences. 

#Analysis#
- Hopper will now treat any detected Ø instances as 0 (zero) preventing labels ending up with Ø symbols which is the default font in some recording programs.
- Hopper will now by default exclude trailing percentages in cue label detection.
- Support for cue-fields formatted as X/YYY (Cue list/Cue number), currently the cue list will be disregarded. 

============
# Version 0.52
18 April 2026

#General#
- Hopper now generates a small thumbnail into the Hopper file and shows video thumbnails in the recent list where possible.
- You can relaunch the onboarding window from the preferences window
- General improvements with show management/ file ordering in sidebar.

#Playback#
- Added toggle in Console control settings under Trigger Console. Re-send fire command on playback resume. Will send the relevant cue each time playback is resumed.
- General show playback fixes including faster switching between videos, bug fixes with renaming videos.

#Licensing#
- FIXED: Hopper clients which cannot phone home will remain active until the license expiry date instead of locking up after 7 days.


============
# Version 0.51
08 April 2026

#General#
- Added Share button to Hopper Menu which will show QR code and quick link to send via Email.


#Playback#
- Triggering of cues now supports recordings with multiple of the same cue (e.g. rehearsals that run the same scene over and over) and will trigger the nearest instance of that cue. 
- Trigger the lighting console in Trigger mode (menu drop-down next to follow console), this will send a CUE X Fire message when you pass cues in the video. Behaviour set in settings under remote-control.
- Trigger console mode also stops console playback when you stop the video in playback mode, behaviour set in settings under remote-control
- After 5 mionutes of inactivity in trigger mode, it will warn you that it is still in trigger mode on next play. This can be disabled for the session.

#Show Management#
- FIXED: Deleting the first video in a performance now deletes the correct video. 
 

#Licensing#
- FIXED: License types only allowed on 1 computer could not activate.

============
# Version 0.5
07 April 2026

#Licensing#
- Added offline license activation and deactivation, users can enter their license code into Hopper and then scan a QR code with their phone to complete activation remotely. 


============
# Version 0.4
05 April 2026

#Onboarding#
- Automated ETC EOS Console discovery supports multiple networks

#Playback#
- New remote control macro - Toggle playback which acts as a play/pause function.

#Licensing#
- Added licensing management including activation, deactivation, remote deactivation.

#Development#
- Development warning removed. This will be managed via specific development licenses in future
- This app is now signed!

============
# Version 0.3
01 April 2026

#Development#
- App will warn that it is a development version and behave as if unlicensed after 14 days

#Licensing#
- Added license enforcement behaviour (no actualy licensing yet)

#Analysis#
- Better support of lines with multiple pieces of data (e.g. cue number and label)
- Live analysis results in cue sidebar
- Cancel now saves current results

#Cue management#  
- You can now re-number cues in the side-bar if there are OCR detection issues by double clicking on the number. If you are having lots of OCR issues please get in touch with support.

#Playback#  
- Pre-roll function allows users to define an amount of time to play from before each cue (e.g. see the 2 seconds leading into a cue)
- 

#Audio#  
- Ability to soloe/mute individual channels, label them
- Ability to enable and disable Auto-level which evens out levels (good for quiet comms channel and loud show audio)
- Ability to hide channels so they do not appear in the audio menu-bar window
- Audio settings are written to all videos assosciated with a show so if you open a video by itself it will keep labels and settings. 
- Spatial Audio now off application-wide

===========

# Version 0.2
27 March 2026

- Initial release.
- Single video file playback synchronised to ETC EOS via UDP OSC.
- Vision OCR frame scanning to build cue → timestamp map.
- `.hopper` sidecar file for storing analysis results alongside the video.
