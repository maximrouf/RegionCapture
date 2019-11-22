# Texture Region Capture (Ver. 2.2.5)
Plugin for Unity 2019.2.12 and higher

> Compatibility with Vuforia 8.3.9

ARCore and ARKit are supported by Unity ARFoundation (You can setup it from the Package Manager)

![Region Capture description](https://raw.githubusercontent.com/maximrouf/RegionCapture/master/Images/RegionCapture.jpg)

How to setup (for Vuforia):

	1. Start a new Unity project

	2. (For Android only) Go to the "Player Settings" -> "Other" -> "Rendering" and set OPENGLES3 in the first line

	3. Go to the "Player Settings" -> "XR Settings" and select "Vuforia AR supported" checkbox

	4. Now you can import the "RegionCapture_2.2.5.unitypackage" into your project

	5. Select "Resources" -> "VuforiaConfiguration" in the "Project View" and paste your licence key in the upper field

	6. Also you need to import the "StonesAndChips.unitypackage" in the "Region_Capture" -> "Markers" 
	
	7. And select it on the "ImageTarget Behaviour" at the "Database" rollout

	8. Then set the "World Center Mode" in the ARCamera settings as "First_Target"

	9. Run the demo-scenes into "Assets" -> "Region_Capture" -> "Scenes" folder


How to use:

	1. Set the custom Scale, Position and Rotation to modify region-size
	
	2. Get Texture from "Render_Texture_Camera" in "PlayMode" - RenderTextureCamera.GetRenderTexture()

	3. Enable the option - "Check if the plane is out of bounds" on the "RegionCapture" GameObject 
	   to get the some scripted Unity Events, if the capturing plane is out of a Camera bounds

	4. If all works fine - switch off Layer "Region_Capture" in : ARCamera -> Camera -> Culling Mask 
	   (or enable the "Hide this layer from ARCamera" checkbox);

	5. You can switch from "Game" to the "Scene" window in PlayMode only after the marker is found.
       	
Available methods:

	RenderTextureCamera.MakeScreen();		//  Call it - if you want to save RegionTexture to localStorage


       	
If you see a shift of the captured image or another bug, please report [here](https://developer.vuforia.com/forum/unity-extension-technical-discussion/region-capture-0)

Bug report should be in the following format:

	1. Unity version
	2. Vuforia version
	3. RegionCapture version
	4. Device name
	5. Device OS version
	6. Orientation of the device (portrait / landscape / both)

If you want to attach a screenshot, please use the image upload service.  ( [for example - https://imgbb.com](https://imgbb.com) )
  
  
  Best Regards, Maxim Rouf
