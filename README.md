# Texture Region Capture (Ver. 1.7.7)
Plugin for Vuforia 5.X & Unity 5.X

Release notes:  

* Global perfomance - 10%

* MultiTarget - added
* StereoMode - fixed

* Shift texture on small ImageTargets in Editor - fixed
* Shift texture on some devices - fixed (not tested!)

* "Hide Android Toolbar" function - moved to RC_Tools
* "Autofocus Camera" function - moved to RC_Tools
* "Marker Background" functuon - updated

* Samples code - updated

* Now you can place RegionCapture prefab into ImageTarget

---------------------------------------------------------------

How to setup:

	1. Create a new layer №20 "Region_Capture"
	2. Drag Prefab into the scene
	3. Set a references (to the game objects) in Prefab


How to use:

	1. Get Texture from "Render_Texture_Camera" in PlayMode - RenderTextureCamera.CameraOutputTexture (look at "Samples" folder)

	2. Set custom Scale, Position, Rotation (with 90-degree increments) to modify region size (disable "Auto Region Size" checkbox);
	
	3. If all works fine - switch off Layer "Region_Capture" in ARCamera > Camera > Culling Mask (or enable "Hide from ARCamera" checkbox);

	4. Enable "Check Marker Position" checkbox, to get state (see console messages) if the marker is out of bounds.

	5. Enable "Color Debug Mode" checkbox, to highlight captured marker.

	6. Enable "Show Texture" checkbox, to draw RenderTexture in GUI.

	7. Add any texture to the "Marker Background" field if you want to overwrite white spots in captured texture.
	
	8. Enable "Autofocus Camera" checkbox, if you want to use autofocus on Android devices.

	9. Enable "Hide Android Toolbar" checkbox, to hide navigation toolbar on devices without physical buttons.


How to IOS build:

	Add AssetsLibrary.framework in XCode project (Expand Link Binary With Libraries and click (+) button)

	PS: AssetsLibrary is deprecated (but still work) in iOS 9.0 and will be replaced to Photos framework next time.



Available methods:

	Region_Capture.RecalculateRegionSize();		//	Call it - if the marker has changed.

	RenderTextureCamera.RecalculateTextureSize();		//	Call it - if the marker or size of renderTexture has changed.

	RenderTextureCamera.MakeScreen();		//	Call it - if you want to save RegionTexture to localStorage.


  Best Regards, Maxim Ruf
