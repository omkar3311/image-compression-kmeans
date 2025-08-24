# 🎨 Image Compression using KMeans  

## 📌 Overview  
With the rapid growth of digital media, storage and bandwidth requirements for images have increased significantly. While traditional compression methods like **JPEG** or **PNG** are effective, this project explores how **Machine Learning (Unsupervised Learning)** can also be applied for image compression.  

We use **K-Means clustering** to reduce the number of unique colors in an image. By grouping similar colors and replacing them with their cluster centroids, the image is reconstructed with fewer colors — achieving compression while maintaining visual quality.  

---

## 🚀 Approach  

1. **Image as Data**  
   - An image is just a collection of pixels.  
   - Each pixel has 3 values: **R (Red), G (Green), B (Blue)**.  
   - Many colors are similar, but stored individually, which increases file size.  

2. **K-Means Clustering**  
   - Each pixel (RGB triplet) is treated as a point in 3D space.  
   - K-Means groups pixels into *k* clusters.  
   - Each cluster is represented by its **centroid color**.  

3. **Reconstruction**  
   - Each pixel is replaced with the centroid color of its cluster.  
   - The new image now has only *k* unique colors.  

4. **Compression Effect**  
   - Instead of storing all original colors, we store:  
     - The *k* centroid colors  
     - A cluster label for each pixel  
   - This reduces storage size while keeping the image visually similar.  

---

## 🎯 Expected Results  

- **Side-by-side comparison**: Original image vs Compressed image  
- **File size difference** before and after compression  
- **Effect of `k`**: trade-off between quality and compression  

---

## 📊 Example  

| Original Image | Compressed (k=16) | Compressed (k=8) |
|----------------|-------------------|------------------|
| ![original](examples/original.png) | ![k16](examples/k16.png) | ![k8](examples/k8.png) |

---

## 🛠️ Installation & Usage  

1. Clone the repository:  
   ```bash
   git clone https://github.com/yourusername/image-compression-kmeans.git
   cd image-compression-kmeans
  
2. Run the Jupyter Notebook:
```bash
jupyter notebook image.ipynb
```
## Requirements

     Python 3.x
     
     NumPy
     
     Matplotlib
     
     scikit-learn
     
     Jupyter Notebook
---
## Author

Developed by **Omkar Waghmare**.  
Aspiring Data Scientist | Passion for ML & Data
