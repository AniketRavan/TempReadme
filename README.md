# TempReadme
# Independent-Cell-Tracker for Directional Studies of Cell Migration
#Synopsis
This is a semi-supervised tracking algorithm written to track cells in phase contrast images using MATLAB's R2015a version. Images undergo binary classification based on pixel intensity and local standard deviation of pixel values. A Support Vector Machine classifier is used for this step. The classifier is automatically trained in every frame using information between successive frames. 
Please note that the algorithm is written for single cell studies and thus only independent cells are tracked. The rate at which images are captured has to be above a certain minimum. The algorithm may give erroneous results if the distance traveled by any cell between two frames is greater than its own dimension. 

#Using the Software
**Load Images**<br/>
![alt tag](https://github.com/oist/Independent-Cell-Tracker/blob/Images/Load.png)<br/>
The software gives best results for phase contrast images.<br/>

**Manual Tracking**<br/>
For studies of directional migration it is highly recommended to use the 'Automatic Tracking' feature since directions of displacement vectors obtained using Manual Tracking can be often unreliable.<br/>
<img src="https://github.com/oist/Independent-Cell-Tracker/blob/Images/ManualTracking1.png" width="420" align="left"/>
<img src="https://github.com/oist/Independent-Cell-Tracker/blob/Images/ManualTracking2.png" width="420" align="right"/>
<br/> <br/> <br/> <br/> <br/> <br/> <br/> <br/> <br/> <br/> <br/> <br/> <br/> <br/>
Also note that you can track only one cell at a time.
<br/>

**Preprocessing**<br/>
Before using the Automatic Thresholding features the images have to be processed for better performance. Use the horizontal filter scrollbar to filter out the background. <br/>
<img src="https://github.com/oist/Independent-Cell-Tracker/blob/Images/Filter1.png" width="420" align="left">
<img src="https://github.com/oist/Independent-Cell-Tracker/blob/Images/Filter2.png" width="420" align="right">
<br/> <br/> <br/> <br/> <br/> <br/> <br/> <br/> <br/> <br/> <br/> <br/> <br/> <br/>
You can also scroll the image quality for efficiency. A lower image quality gives better speed, but also compromises the accuracy of segmentation.

**Automatic Tracking** <br/>
On clicking the Automatic Tracking button the user is prompted to select the centroids of cells they wish to track. Please be careful to click near centroids of independent cells only.<br/>
<img src="https://github.com/oist/Independent-Cell-Tracker/blob/Images/Automatic1.png" width="420" align="left">
<img src="https://github.com/oist/Independent-Cell-Tracker/blob/Images/Automatic2.png" width="420" align="right">
<br/> <br/> <br/> <br/> <br/> <br/> <br/> <br/><br/> <br/><br/><br/><br/> <br/> <br/>
Centroids of cells being tracked are marked with a green cross ('x'). Cells at the border of the screen are ignored. 

**Export Data** <br/>
The displacement vectors of tracked cells are exported to excel in the form of two rows for 'distance' and 'theta'.
