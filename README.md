# Unity_Stats_VR_HUD

Unity Statistics VR HUD and Debug Tool

Download package here: 

Statistics HUD
This tool was created for quick and easy issue identification and optimization inside VR, it aims to make the process easier while using HMDs. The Unity Editor provides useful information in its dropdown “Stats” window, however this overlay is not visible in VR. This results in having to remove the headset or partially wearing it to see these useful real-time values. This tool takes the most important values: FPS, batches, set-pass calls, tris and puts them in a world space canvas so they can be monitored easily in real-time while in VR. It also includes additional useful features for debugging. 

The display as seen here matches closely that values shown in the stats window. Most importantly the FPS as displayed in the stats window attempts to emulate the FPS of a built project. It excludes the editor windows and only accounts for the game window in Unity to do this, standard approaches to creating FPS counters in Unity do not account for this. The FPS value shown on the HUD uses Unity Statistics to display the “Estimated FPS for Build” giving an estimation of the built FPS without having to do a length build to see this in VR.

In the inspector an FPS threshold can be set, such as 60 FPS, when the estimated game FPS falls bellow this the FPS value will go red giving the user an indication that there has been a drop in FPS. 

Profiler
Generally, the Profiler is hooked into Dev builds, this of course requires building the project to look for issues. This tool has been optimized to work alongside the profiler in the editor view, without building.

When using the Profiler, the HUD “estimated FPS” will be affected by this process, unlike other editor windows.

When working with the profiler it is recommended to use the “Autoclear Profiler” option. This will clear the profiler buffer after a certain point, instead of saving a log of every frame. This is to stop large FPS drops and performance issues caused by the Profiler chugging through a large amount of frame data. 

Autopause
Pressing ‘A’ on the Oculus Touch controller will toggle the Autopause feature, this will automatically pause the game when FPS drops below your set FPS Threshold. This will allow easy checking of the HUD and Profiler without rushing to pause and check the data. 
After unpausing the game Autopause will be disabled, simply press A to activate it again. It is recommended to set an FPS threshold lower that the traditional 60FPS as the profiler may affect estimated FPS and this will only pause the game to catch large spikes.

Summary

•	World space real-time Unity stats.
•	Profiler optimization.
•	FPS threshold for FPS drop notifications.
•	FPS Autopause to allow easy removal of HMD and profiler spike checking.
