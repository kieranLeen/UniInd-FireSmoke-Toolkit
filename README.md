### UniInd-FireSmoke-Toolkit
#### Official toolkit for the paper Beyond Pixels: A Topology-Aware Framework for Smoke Analysis on Multimodal Industrial Benchmark
#### Please follow the guide to use the tool for downstream industrial Fire-Smoke Analysis tasks
1. GUI Hierarchy and Structure:
The GUI consists of two main levels, each serving distinct purposes:
	First-level Main Window: 
   - The interface where the user selects input and output directories and determines the type of analysis to be conducted (image-based or video-based). For the current version, image-based analysis refers to flare and smoke detection, segmentation, and measurements.
  
     
<p align="center">
  <img src="https://github.com/user-attachments/assets/6423970d-ae8d-422b-952f-92aa400a2541 " alt="image" />
</p>

	Second-level Main Window: 
   - Displays the processed results across four consoles. These consoles offer additional interaction through sub-windows when double-clicked, providing more detailed data such as segmentation masks, color analysis, flare-smoke ratio, flare orientation.

<p align="center">
  <img src="https://github.com/user-attachments/assets/ef2202aa-8033-4ff0-a2e6-e27e45b32ecb " alt="image" />
</p>


1.1 First-level Main Window
The ‘First-level Main Window’ is the starting point of the GUI, where users set up the analysis by selecting directories and defining the analysis scope. This interface includes:
- Directory Selection:
  - Users input the directory paths for images, videos, and output folders through text fields.
  - The directory selection buttons (such as "Select Image Directory," "Select Video Directory," "Select Output Directory" which are marked in red box in the attached screenshot), these buttons can open file dialogs for easy path selection (marked in green box).
 
    
 ![image](https://github.com/user-attachments/assets/9c834282-20ef-4334-bbe1-07f9122c3be6)

- Analysis Type Selection (marked in red box):
  - The user can start image-based or video-based analysis by clicking the respective buttons. 
  - The "Start Image Auto-labelling" button initiates image-based object detection and segmentation.
  - The "Split Video to Frames" button extracts frames from video files for analysis.
  - The "Start Analysis" button runs gas flare analysis on videos.
 
    
 ![image](https://github.com/user-attachments/assets/eb5aca52-b870-4af9-9b7a-7a01114ee313)

- Log Console (marked in green box):
  - The log console displays real-time progress of the tasks, including how many images or frames have been processed and whether the tasks completed successfully. If the user selects ‘split video to frames’ service, the Log Console will display how many frames are split from the raw video and also the collapsed time.

1.2 Second-level Main Window
The ‘Second-level Main Window’ opens once the analysis is completed. It contains four consoles, each displaying specific aspects of the processed data. These consoles provide users with an overview of the analysis, while sub-windows can be accessed for more detailed information.
- Console 1: Original Image - Displays the raw, unprocessed image from the input directory.
- Console 2: Detection Results - Shows bounding boxes around detected objects (flame, smoke) and presents metrics such as flame angle, smoke/flare ratio, flame size, and smoke size.
- Console 3: Segmentation (Flame and Smoke) - Highlights flame and smoke areas with colored masks (red for flame, blue for smoke).
- Console 4: Flame Orientation - Shows a graphical representation of the flame’s angle and direction.

  
![image](https://github.com/user-attachments/assets/af75a0fb-5e0f-46d6-8522-3cecdcc3d9f4)


2. Sub-windows Triggered by Consoles
The sub-windows are detailed information windows that open when the user double-clicks on specific consoles. Each sub-window provides additional insights into the corresponding data.
2.1	Sub-window for Segmentation (Triggered from Console 3)
By double-clicking on the Segmentation Console (Console 3), a sub-window opens to provide a more detailed view of the segmentation process. This includes:

- Flare Mask - The segmentation results showing the areas detected as flames.
- Smoke Mask - The segmentation results showing the areas detected as smoke.
This double-click action leads to a sub-window similar to the following visualization:

![image](https://github.com/user-attachments/assets/60c42e64-9eda-422d-b553-88466374bcd1)


2.2	Sub-window for Detailed Metrics (Triggered from Console 4)

By double-clicking on the Flame Orientation Console (Console 4), another sub-window appears, providing the following detailed metrics (Marked in Red box):

- Flare/Smoke Ratio- A graphical representation of the flare-to-smoke ratio, flare-to-image ratio, and smoke-to-image ratio.
- Color Analysis - A histogram showing the distribution of color intensity across red, green, and blue channels for the image.
- Flame and Smoke Sizes - The calculated sizes of the flame and smoke regions.
- Flame Angle - The angle of the flame, with details on how the flame is oriented in the image.+
An example of this sub-window with detailed metrics is shown below:

![image](https://github.com/user-attachments/assets/bcdc0a40-a38d-44aa-9454-398121572ffa)

 

