# 🛰️ AI-Based Geospatial Rooftop Classification

![Output](outputs/roof_classification_result.png)

---

## 📌 Overview
This project focuses on extracting and classifying rooftop types from high-resolution drone orthophotos using geospatial data and deep learning. It integrates raster satellite imagery (TIFF) with vector shapefile annotations (SHP) to automatically generate labeled datasets and perform semantic segmentation.

---

## 🚀 Key Features
- 🏠 Multi-class rooftop classification (4 roof types + background)
- 🏙️ Built-up area segmentation using UNet
- 🗺️ Automatic mask generation from shapefiles (no manual labeling)
- 🧠 Deep learning using UNet (ResNet34 encoder)
- 📊 Clean visual outputs for interpretation

---

## 🧠 Methodology
Drone Orthophoto (TIFF)  
↓  
Tile Generation (256×256)  
↓  
Shapefile (Built_Up_Area_type.shp)  
↓  
Rasterization → Multi-class Masks  
↓  
Dataset Creation (Image + Mask pairs)  
↓  
UNet Model Training  
↓  
Roof Type Classification Output  

---

## 📂 Project Structure
Ai_HAckathon/  
│  
├── Ai_HAckathon.ipynb         # Main Colab notebook  
├── outputs/  
│   └── roof_classification_result.png  
└── README.md  

---

## 📊 Dataset Details
- Input: Drone orthophotos (.tif)  
- Annotations: Shapefile (Built_Up_Area_type.shp)  
- Tile Size: 256 × 256  

### Classes:
0 → Background  
1 → Roof Type 1  
2 → Roof Type 2  
3 → Roof Type 3  
4 → Roof Type 4  

---

## 🛠️ Tech Stack
Python  
Google Colab  
PyTorch  
segmentation-models-pytorch  
Rasterio  
GeoPandas  
OpenCV  
NumPy  
Matplotlib  

---

## 🖼️ Output
The output visualization shows:  
Left → Original drone tile  
Right → Roof type segmentation mask (color-coded)  

Each color represents a different roof type class.

---

## 📈 Current Progress
- ✅ Built-up area segmentation model completed  
- ✅ Roof-type dataset generated using shapefiles  
- ✅ Multi-class masks verified and visualized  
- 🔄 Roof classification model training (next step)  
- ⏳ Water body and infrastructure detection planned  

---

## 🎯 Future Improvements
- Train full multi-class rooftop classification model  
- Add water body and infrastructure detection  
- Improve accuracy using augmentation  
- Deploy model for real-time usage  

---

## 💡 Key Highlights
- Uses real-world geospatial data  
- Fully automated labeling pipeline  
- Scalable for large-area mapping  
- Clean and interpretable outputs  

---

## 👨‍💻 Author
Nithish Kannan  

---

## 📌 Note
This project is developed as part of a Geospatial AI Hackathon focusing on real-world mapping, infrastructure detection, and environmental analysis.
