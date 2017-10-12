# Texture Region Capture (Ver. 2.0)
Plugin for Unity 2017.2 and higher

Compatibility with Vuforia 6.5 - 7.X
 (ARCore and ARKit - Coming soon)

---------------------------------------------------------------

How to setup:

	1. Create a new Unity project
	2. Go to "Project setings -> Player" and select the "XR Settings -> Vuforia" checkbox
	3. Then click in the upper menu to "GameObject -> Vuforia -> ARCamera" (to import Vuforia files into the project)
	4. Select "Resources -> VuforiaConfiguration" in the "Project View" and paste your licence key in the upper field
	5. Now you can test the demo-scenes into "Assets -> Region_Capture -> Examples"


How to use:

	1. Set the custom Scale, Position, Rotation (with 90-degree increments) to modify region-size
	
	2. Get Texture from "Render_Texture_Camera" in "PlayMode" - RenderTextureCamera.GetRenderTexture()

	3. Enable "Check if the plane is out of bounds" checkbox to get the Events, if the capturing plane is out of a Camera bounds

	4. If all works fine - switch off Layer "Region_Capture" in : ARCamera > Camera > Culling Mask (or enable the "Hide this layer from ARCamera" checkbox);


Available methods:

	Region_Capture.RecalculateRegionSize();		//  Call it - if the marker has changed

	RenderTextureCamera.RecalculateTextureSize();	//  Call it - if the marker or size of renderTexture has changed

	RenderTextureCamera.MakeScreen();		//  Call it - if you want to save RegionTexture to localStorage


  Best Regards, Maxim Rouf
