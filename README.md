# YOLOv8-LSH
# YOLOv8-LSH: A Lightweight Helmet Detection Algorithm with Enhanced Accuracy and Efficiency

This repository provides the official implementation of our paper submitted to *The Visual Computer*.

## 🔗 Paper
"This code is directly related to our manuscript currently submitted to *The Visual Computer*. If you find this work helpful, please consider citing our paper."

## 🚀 Highlights
- Lightweight feature extraction using KWConv and C2f-KW
- Efficient detection head (SCDH)
- Wise-IoU loss for improved accuracy
- 63% FLOPs reduction, 19% fewer parameters

## **Download the project zip file** from GitHub:  
1.  [Click here to download the code package]
2. **Open and read** the `README.md` file inside the root directory to understand the usage instructions and setup process.
3. **Install the required environment dependencies** using the provided readme.md file:

## 📁 Dataset Configuration
Data Availability Statement:The dataset used in this study is publicly available at: https://github.com/zhong110020/Safety-Helmet-Wearing-Dataset

Edit the `dataset/data.yaml` file and specify the correct paths to your dataset:

train: dataset/images/train
val: dataset/images/val
nc: 2
names: ['helmet', 'head']

## 🧠 Model Loading

The model configuration is loaded using the following code in Python:

from ultralytics import YOLO

model = YOLO(r'ultralytics/cfg/models/v8n/yolov8-LSH.yaml')
## 🏃‍♂️ Run Training
After completing the model and dataset configuration, navigate to the project root directory and run:

python train.py --data dataset/data.yaml --cfg ultralytics/cfg/models/v8n/yolov8-LSH.yaml
## Evaluation

python val.py --weights ultralytics/weights/YOLOv8-LSH.pt
