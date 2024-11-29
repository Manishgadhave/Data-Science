# Object Detection Using YOLOv5 🚀

This project demonstrates object detection on images and videos using the YOLOv5 model. YOLOv5 is a state-of-the-art object detection algorithm capable of identifying and localizing objects in real-time.

## Steps Performed

### 1️⃣ Clone the YOLOv5 Repository
The YOLOv5 repository from Ultralytics is cloned for access to the pre-trained model and related utilities.
```bash
!git clone https://github.com/ultralytics/yolov5.git
```

### 2️⃣ Change Directory
Navigate to the `yolov5` directory to access necessary scripts and configurations.
```bash
%cd yolov5/
```

### 3️⃣ Install Dependencies
Install all required dependencies listed in the `requirements.txt` file.
```bash
!pip install -U -r requirements.txt
```

### 4️⃣ Object Detection on Images
- Place your images in the `inference/images/` folder.
- Run the detection script:
  ```bash
  !python detect.py --source inference/images/your_image.jpg --weights yolov5s.pt --conf 0.4
  ```
- Detected objects are saved in the `runs/detect/exp` folder.

#### Display Detected Image in Colab
```python
import cv2
import matplotlib.pyplot as plt

image = cv2.imread("/content/yolov5/runs/detect/exp7/zidane.jpg")
height, width = image.shape[:2]
resized_image = cv2.resize(image, (3*width, 3*height), interpolation=cv2.INTER_CUBIC)

plt.figure(figsize=(18, 10))
plt.axis("off")
plt.imshow(cv2.cvtColor(resized_image, cv2.COLOR_BGR2RGB))
plt.show()
```

### 5️⃣ Object Detection on Videos
- Place your video files in the `inference/videos/` folder.
- Run the detection script:
  ```bash
  !python detect.py --source inference/videos/your_video.mp4 --weights yolov5s.pt --conf 0.4
  ```
- Processed videos are saved in the `runs/detect/exp` folder.

#### Display Detected Video in Colab
```python
import cv2
import matplotlib.pyplot as plt
from IPython.display import clear_output

video_path = "/content/yolov5/runs/detect/exp8/street.mp4"
cap = cv2.VideoCapture(video_path)

while cap.isOpened():
    ret, frame = cap.read()
    if not ret:
        break
    plt.imshow(cv2.cvtColor(frame, cv2.COLOR_BGR2RGB))
    plt.axis("off")
    plt.show()
    clear_output(wait=True)

cap.release()
```

## Results
- Detected objects are saved in the `runs/detect/` folder.
- You can view processed images and videos directly in your local directory or within Colab.

## Requirements
- Python 3.7+
- PyTorch
- OpenCV
- Matplotlib

## Acknowledgements
This project uses [YOLOv5 by Ultralytics](https://github.com/ultralytics/yolov5).
