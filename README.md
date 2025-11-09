# Vehicle Detection using YOLOv8 🚗

This project trains a **custom YOLOv8 object detection model** to detect various types of vehicles such as cars, buses, trucks, and motorcycles.

---

## 📂 Dataset
- Total images: 5,626
- Classes (11 total):
  - pickup_truck
  - car
  - articulated_truck
  - bus
  - motorized_vehicle
  - work_van
  - single_unit_truck
  - pedestrian
  - bicycle
  - non-motorized_vehicle
  - motorcycle

Data was preprocessed and converted to YOLO format using bounding box annotations from `labels.csv`.

---

## 🧠 Model
Trained using **YOLOv8n** (Nano model) on Google Colab with a Tesla T4 GPU.

| Metric | Value |
|:--------|:--------|
| Precision | 0.54 |
| Recall | 0.30 |
| mAP50 | 0.33 |
| mAP50–95 | 0.21 |

The model improves significantly with 50+ epochs.

---

## 🚀 Results
Example inference image:

![Sample Detection](samples/sample_detection.jpg)

---

## 🧾 How to Run

### 1️⃣ Install Dependencies
```bash
pip install -r requirements.txt


from ultralytics import YOLO
model = YOLO('best.pt')
results = model.predict('path_to_image.jpg', conf=0.4, save=True)


yolo train data=dataset.yaml model=yolov8n.pt epochs=50 imgsz=640


🧑‍💻 Author

Created by Kiran Kumar Duggirala — as part of Object Detection Project

