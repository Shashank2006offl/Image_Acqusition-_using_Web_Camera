# Image Acquisition using Web Camera

### Name : SHASHANK R
### Register No : 212223230205

## Aim :
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm :
### Step 1 :

Import the cv2 and numpy package.
<br>
### Step 2 :
Read the Video frame using the cv2.VideoCapture(0)
<br>

### Step 3 :
Write the image using imwrite().
<br>

### Step 4 :
Display the frame using the imshow().
<br>

### Step 5 :
Divide the frame into halves and assign the smaller frame and Rotate the frame using the cv2.rotate().
<br>

## Program:
``` Python
### Developed By:
### Register No:

## i) Write the frame as JPG file

import cv2 
cap = cv2.VideoCapture (0) 
frame_number = 0 # Initialize frame number 
while frame_number < 5: 
    ret, frame = cap.read() 
    cv2.imshow('frame', frame) 
    # Save frame as JPG file 
    cv2.imwrite(f"frame_{frame_number}.jpg", frame) 
    frame_number += 1 
    if cv2.waitKey(1) & 0xFF == ord('q'): 
        break 
cap.release() 
cv2.destroyAllWindows()


## ii) Display the video
import cv2 
cap = cv2.VideoCapture (0) 
while True: 
    ret, frame = cap.read() 
    cv2.imshow('Video', frame) 
    if cv2.waitKey(1) & 0xFF == ord('q'): 
        break 
cap.release() 
cv2.destroyAllWindows() 

## iii) Display the video by resizing the window
import cv2 
cap = cv2.VideoCapture(0) 
# Create a resizable window 
cv2.namedWindow('Video', cv2.WINDOW_NORMAL) 
while True: 
    ret, frame = cap.read() 
    cv2.imshow('Video', frame) 
    # Resize the window 
    cv2.resizeWindow('Video', 100, 200) 
    if cv2.waitKey(1) & 0xFF == ord('q'): 
        break 
cap.release() 
cv2.destroyAllWindows()


## iv) Rotate and display the video

# import cv2 
cap = cv2.VideoCapture (0) 
# Define the rotation angle (in degrees) 
rotation_angle = 90 
while True: 
    ret, frame = cap.read() 
    # Rotate the frame 
    rotated_frame = cv2.rotate(frame, cv2.ROTATE_90_CLOCKWISE) 
    cv2.imshow('Rotated Video', rotated_frame) 
    if cv2.waitKey(1) & 0xFF == ord('q'): 
        break 
cap.release() 
cv2.destroyAllWindows()

```
## Output


### ii) Display the video
</br>
![image](https://github.com/user-attachments/assets/7c5faa03-fcf8-47d2-9a10-0f5a0035521d)

</br>


### iii) Display the video by resizing the window
</br>
![Screenshot 2025-03-28 111936](https://github.com/user-attachments/assets/1b4f33f7-a18a-4d0d-b5fe-1d744a2d6c87)
</br>


### iv) Rotate and display the video
</br>
![Screenshot 2025-03-28 112750](https://github.com/user-attachments/assets/174c7677-5930-42de-b6b4-f530318b6f99)
</br>





## Result:
Thus the image is accessed from webcamera and displayed using openCV.
