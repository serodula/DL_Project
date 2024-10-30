__Project Title - Parking Space Detection System__


__Overview__
The Parking Lot Occupancy Detection Project deals with the problem of detecting the occupancy of a parking lot using video analysis. Displaying the status of occupied or vacant spots, tracking the duration of time a vehicle has stayed, and sending notifications on overstayed vehicles fall into its domain. Having an original solution with OpenCV processing and text overlay in CVZone, this tool performs a strong and effective methodology on parking management.


__Features__<br/>
__Real-Time Detection:__ This continuously monitors every car parking space to identify whether it is free or occupied.
__Occupancy tracking:__ It estimates the time each vehicle spends in a parking space and automatically provides notifications if it detects an overstay.
__Visual Feedback:__ It shows the status of parking directly onto the video by using color-coded indications.
__Statistics Display:__ This displays how many spaces are occupied and unoccupied at any moment in time.


__Getting Started__
__Prerequisites__
__Python 3.6+__
__OpenCV: pip install opencv-python__
__CVZone: pip install cvzone__
__NumPy: pip install numpy__


__Implementation Details__
It works as follows: 

__Video Frame Processing:__ It converts each frame from the video feed to grayscale, blurs it, and thresholds it so that the parked vehicles stand out.
__Parking Spot Detection:__ Crop the ROI of each parking space and analyze it. The count of the pixels will define whether the space is vacant or occupied.
__Occupancy and Overstay Tracking:__ A dictionary can keep a record of each vehicle's entry timing. If a vehicle exceeds the threshold time set, an "Overstay" alert can be indicated.
__User Interface:__ Visual indicators of parking status; statistics of occupied/vacant spaces are calculated and updated automatically.


__Acknowledgments__
__OpenCV: https://opencv.org/__
__CVZone: https://github.com/cvzone/cvzone__
