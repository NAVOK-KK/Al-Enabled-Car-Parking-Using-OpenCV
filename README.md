# AI ENABLED CAR PARKING SYSTEM

# Team Members:
* Mouleeshwaran B
* Kalaikovan P
* Hemalatha M
* Anitha S


Car parking is a common problem faced by drivers in busy urban areas. For example, imagine you are driving to a shopping mall during peak hours. As you approach the mall, you notice that the parking lot is full, and several other cars are circling around looking for available spots.

You join the queue of cars, hoping to find an available spot soon. However, as time passes, you realize that the parking lot is overcrowded, and it's becoming increasingly difficult to find a spot. You start to feel frustrated and anxious, knowing that you might be late for your appointment or miss out on a great shopping opportunity.

AI-enabled car parking using OpenCV is a computer vision-based project that aims to automate the parking process. The project involves developing an intelligent system that can identify empty parking spaces and it gives the count of available parking spots. The system uses a camera and OpenCV (Open Source Computer Vision) library to capture live video footage of the parking lot.



# Coding Explanation: 
1. Import the necessary libraries such as **cv2**, **pickle**, **cvzone** and **numpy**.
2. Load the video feed from the file **carPark.mp4** using **cv2.VideoCapture()**.
3. Load the positions of the parking spaces from the file **CarParkPos** using **pickle.load()**.
4. Set the width and height of each parking space to 107 and 48 pixels respectively.
5. Define a function called **checkParkingSpace()** which takes an image as input and loops through each position in the list of parking space positions.
6. Crop the image to the size of a parking space using array slicing.
7. Count the number of non-zero pixels in the cropped image using **cv2.countNonZero()**.
8. If the count is less than 900, mark it as a free parking space with a green rectangle using **cv2.rectangle()** and increment the counter for free parking spaces.
9. Otherwise, mark it as an occupied parking space with a red rectangle.
10. Display the number of free parking spaces on the top left corner of the video feed using **cvzone.putTextRect()**.
11. Loop through each frame in the video feed and apply image processing techniques such as Gaussian blur, adaptive thresholding, median blur and dilation to detect parking spaces using **cv2.cvtColor()**, **cv2.GaussianBlur()**, **cv2.adaptiveThreshold()**, **cv2.medianBlur()** and **cv2.dilate()** respectively.
12. Call the function **checkParkingSpace()** on each processed frame to detect free and occupied parking spaces.
13. Display the video feed with marked parking spaces and number of free parking spaces using **cv2.imshow()**.
14. Wait for 10 milliseconds before displaying the next frame using **cv2.waitKey()**.

