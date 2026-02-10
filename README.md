
Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
<br>

### Step 2:
<br>

### Step 3:
<br>

### Step 4:
<br>

### Step 5:
<br>

## Program:

### Developed By: Mubarak R
### Register No: 212224220066

## i) Write the frame as JPG file
```
import cv2
import matplotlib.pyplot as plt
from IPython.display import clear_output
import time

cap = cv2.VideoCapture(0)
ret, frame = cap.read()
if ret:
    cv2.imwrite("captured_frame.jpg", frame)
cap.release()

captured_image = cv2.imread('captured_frame.jpg')

plt.imshow(captured_image[:,:,::-1])
plt.title('Captured Frame')
plt.axis('off')
plt.show()

```

## ii) Display the video

```
# Display the video

cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break

    frame_rgb = cv2.cvtColor(frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()

```

## iii) Display the video by resizing the window

```

# Display the video by resizing the window

cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break

    resized_frame = cv2.resize(frame, (100, 150))
    frame_rgb = cv2.cvtColor(resized_frame, cv2.COLOR_BGR2RGB)

    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()

    time.sleep(0.05)

cap.release()


```




## iv) Rotate and display the video

```
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break

    rotated_frame = cv2.rotate(frame, cv2.ROTATE_90_CLOCKWISE)
    frame_rgb = cv2.cvtColor(rotated_frame, cv2.COLOR_BGR2RGB)

    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()

    time.sleep(0.05)

cap.release()

```
## Output

### i) Write the frame as JPG image
<img width="587" height="456" alt="image" src="https://github.com/user-attachments/assets/0a9fc59a-2eb9-460f-85ac-82201b63b074" />



### ii) Display the video
<img width="564" height="425" alt="image" src="https://github.com/user-attachments/assets/af7c05dd-0de1-42ad-84b5-89d13488e17e" />


### iii) Display the video by resizing the window
<img width="277" height="418" alt="image" src="https://github.com/user-attachments/assets/f0d5c1e3-fd50-44e8-9946-4cba20fcc7f4" />



### iv) Rotate and display the video
<img width="313" height="422" alt="image" src="https://github.com/user-attachments/assets/e1b3c2be-7e4c-4852-8704-49d1b63b17f9" />





## Result:
Thus the image is accessed from webcamera and displayed using openCV.
