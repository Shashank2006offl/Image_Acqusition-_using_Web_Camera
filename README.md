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
### Developed By: Shashank R
### Register No:212223230205

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


### i) Display the video
![image](https://github.com/user-attachments/assets/a5a837d3-4048-49a5-b7d2-4086a2fda565)

### ii) Display the video by resizing the window
![image](https://github.com/user-attachments/assets/32b37177-e7c4-4d1c-b8cf-dab134cf3120)

### iii) Rotate and display the video
![image](https://github.com/user-attachments/assets/8c455b66-1042-4ed3-b109-d80c0fc9534a)

## Result:
Thus the image is accessed from webcamera and displayed using openCV.
