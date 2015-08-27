# Texture Region Capture (Ver. 1.6.0)
Plug-in for Vuforia 5.0.5

How to setup:

	1. Create a new layer №20 "Region_Capture"
	2. Drag Prefab into the scene
	3. Set a references (to the game objects) in Prefab

How to use:

	1. Get Texture from "Render_Texture_Camera" in PlayMode

	2. Set custom Scale, Position, Rotation (with 90-degree increments) to modify region size (disable "Auto Region Size" checkbox);
	
	3. If all works fine - switch off Layer "Region_Capture" in ARCamera > Camera > Culling Mask (or enable "Hide from ARCamera" checkbox);

	4. Enable "Autofocus Camera" checkbox, if you want to use autofocus on Android devices.

	5. Enable "Hide Android Toolbar" checkbox, to hide navigation toolbar in some devices without physical buttons.

	6. Enable "Show Texture" checkbox, to draw RenderTexture in GUI.

	7. Set value from 0 to 10 in "Reduce Noise" range to reduce color noise in capturing image.

	8. Enable "Check Marker Position" checkbox, to get state (see console messages) if the marker is out of bounds.

Available methods:

Region_Capture.RecalculateRegionSize();	//	Call it - if the marker has changed.

RenderTextureCamera.RecalculateTextureSize();	//	Call it - if the marker or size of renderTexture has changed.

RenderTextureCamera.MakeScreen();	//	Call it - if you want to save RegionTexture to localStorage.


  Best Regards, Maxim Ruf
