# Texture Region Capture (Ver. 2.0.9)
Plugin for Unity 2017 and higher

> Compatibility with Vuforia 6.X - 7.X

> ARCore & ARKit - Coming soon

EasyAR is not supported. ([A special version for EasyAR is here](https://drive.google.com/uc?id=1-8_fsyE8pKoK_0zPuoJRveJAlNCk5feo&export=download))

![Region Capture description](https://raw.githubusercontent.com/maximrouf/RegionCapture/master/Images/RegionCapture.jpg)

How to setup:

	1. Start a new Unity project

	2. Open the Layers-tab in "Project settings -> Tags and Layers" and set the "Layer №20" name as "Region_Capture" 

	3. Go to "Project settings -> Player" and select the "XR Settings -> Vuforia" checkbox

	4. Then click in the upper menu to "GameObject -> Vuforia -> ARCamera" (to import Vuforia files into the project)

	5. Now you can import the "RegionCapture_2.0.unitypackage" into your project

	6. Select "Resources -> VuforiaConfiguration" in the "Project View" and paste your licence key in the upper field

	7. Also you need to enable "Load StonesAndChips" checkbox in the "Datasets" rollout and click "Activate"

	8. Then set the "World Center Mode" in the ARCamera settings as "First_Target"

	9. Run the demo-scenes into "Assets -> Region_Capture -> Examples"


How to use:

	1. Set the custom Scale, Position and Rotation to modify region-size
	
	2. Get Texture from "Render_Texture_Camera" in "PlayMode" - RenderTextureCamera.GetRenderTexture()

	3. Enable the option - "Check if the plane is out of bounds" on the "RegionCapture" GameObject 
	   to get the some scripted Unity Events, if the capturing plane is out of a Camera bounds

	4. If all works fine - switch off Layer "Region_Capture" in : ARCamera -> Camera -> Culling Mask 
	   (or enable the "Hide this layer from ARCamera" checkbox);

	5. You can switch from "Game" to the "Scene" window in PlayMode only after the marker is found.
       	
Available methods:

	Region_Capture.RecalculateRegionSize();		//  Call it - if the marker has changed

	RenderTextureCamera.RecalculateTextureSize();	//  Call it - if the marker or size of renderTexture has changed

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
