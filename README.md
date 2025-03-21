# **Synthetic Satellite Image Generation Using Diffusion Models**  

This Jupyter Notebook demonstrates the use of **diffusion models** to generate high-quality **synthetic satellite images** for remote sensing applications, including:  
- **Disaster Monitoring** (wildfires, floods, hurricanes)  
- **Super-resolution Image Enhancement**  
- **Semantic Segmentation for Land Classification**  

---

### **📂 File Information**  
📜 **Notebook Name:** `synthetic_satellite_diffusion.ipynb`  
🔹 **Purpose:** Train a diffusion model (Stable Diffusion / DDPM / LDM) to generate synthetic satellite images.  
🔹 **Dataset Used:** **Sentinel-2 satellite imagery (15 days of data)**  

---

### **🛠 Setup & Dependencies**  

#### **1️⃣ Install Required Libraries**  
Run the following command in a cell:  
```python
!pip install torch torchvision diffusers transformers datasets matplotlib numpy opencv-python
```

#### **2️⃣ Load Dataset**  
- Downloads **Sentinel-2** images.  
- Applies **preprocessing**: resizing, normalization, spectral transformations.  

#### **3️⃣ Train Diffusion Model**  
- Implements **forward process** (adding noise to real images).  
- Implements **reverse process** (denoising to generate new images).  

#### **4️⃣ Generate & Evaluate Synthetic Images**  
- Uses **FID (Fréchet Inception Distance) and LPIPS (Perceptual Similarity Score)** to measure quality.  
- Visualizes generated **disaster and normal condition** satellite images.  

---

### **🚀 How to Run This Notebook**  

1️⃣ **Open in Jupyter / Google Colab**  
- Run all cells **sequentially** to train and generate images.  
- Modify hyperparameters like **learning rate, noise steps, and batch size** in the training section.  

2️⃣ **Generate Synthetic Images**  
- After training, run the last cell to generate satellite images.  

---

### **📌 Next Steps**
- Fine-tune the model using additional spectral bands.  
- Implement a **conditional diffusion model** for disaster-specific image generation.  
- Experiment with **Latent Diffusion Models (LDM)** for better efficiency.  
