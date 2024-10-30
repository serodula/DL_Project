# __Project Title - Parking Space Detection System__


### __Overview__<br/>
The Parking Lot Occupancy Detection Project deals with the problem of detecting the occupancy of a parking lot using video analysis. Displaying the status of occupied or vacant spots, tracking the duration of time a vehicle has stayed, and sending notifications on overstayed vehicles fall into its domain. Having an original solution with OpenCV processing and text overlay in CVZone, this tool performs a strong and effective methodology on parking management.


### __Features:__<br/>
__Real-Time Detection:__ This continuously monitors every car parking space to identify whether it is free or occupied.<br/>
__Occupancy tracking:__ It estimates the time each vehicle spends in a parking space and automatically provides notifications if it detects an overstay.<br/>
__Visual Feedback:__ It shows the status of parking directly onto the video by using color-coded indications.<br/>
__Statistics Display:__ This displays how many spaces are occupied and unoccupied at any moment in time.<br/>


## __Getting Started__<br/>

### __Prerequisites__<br/>

__Python 3.6+__<br/>
__OpenCV:__ pip install opencv-python<br/>
__CVZone:__ pip install cvzone<br/>
__NumPy:__ pip install numpy<br/>



### __Implementation Details__<br/>
It works as follows: <br/>
__Video Frame Processing:__ It converts each frame from the video feed to grayscale, blurs it, and thresholds it so that the parked vehicles stand out.<br/>
__Parking Spot Detection:__ Crop the ROI of each parking space and analyze it. The count of the pixels will define whether the space is vacant or occupied.<br/>
__Occupancy and Overstay Tracking:__ A dictionary can keep a record of each vehicle's entry timing. If a vehicle exceeds the threshold time set, an "Overstay" alert can be indicated.<br/>
__User Interface:__ Visual indicators of parking status; statistics of occupied/vacant spaces are calculated and updated automatically.<br/>


### __Acknowledgments__<br/>

__OpenCV: https://opencv.org/__<br/>
__CVZone: https://github.com/cvzone/cvzone__<br/>
