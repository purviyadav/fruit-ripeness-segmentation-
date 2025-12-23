
 **ABSTRACT**
Fruit quality inspection is essential in supply chains and retail markets. Manual ripeness checking is time-consuming and subjective. This project applies color-based image segmentation using K-Means clustering to detect fruit ripeness automatically. Banana and apple images in raw, ripe, and overripe conditions were analyzed. Results show that ripe pixel percentage decreases and overripe percentage increases as fruit becomes older, proving the effectiveness of the proposed method.

**1. INTRODUCTION**
Fruit ripeness influences taste, texture, nutrition, and commercial value.  
Traditional visual inspection lacks accuracy and consistency.

Computer Vision enables automated, objective ripeness detection.  
This work uses **HSV color segmentation** to evaluate fruit condition.

 **2. LITERATURE REVIEW**
- **Image Segmentation:** Separates objects from background using pixel similarity  
- **HSV Color Space:** Preferred over RGB for fruit color analysis  
- **K-Means Clustering:** Groups pixels into K clusters minimizing variability  

Related research suggests color features effectively identify ripeness level.

 **3. PROBLEM DEFINITION**
To design a system that automatically detects ripeness level from fruit images using unsupervised clustering.

**4. OBJECTIVES**
- Segment fruit images based on color
- Identify clusters corresponding to ripeness stages
- Calculate ripe vs. overripe pixel distribution
- Validate effectiveness using real images

**5. METHODOLOGY**

**Block Diagram:**
**Steps:**
1. Capture images in varying ripeness states  
2. Resize to 256×256 pixels  
3. Convert BGR → HSV  
4. K=3 clusters generated using pixel values  
5. Each cluster mapped to ripe / overripe / background  
6. Compute ripeness %  
7. Display outputs (plots + processed image)

**6. IMPLEMENTATION DETAILS**
- Language: Python  
- Libraries: OpenCV, NumPy, Matplotlib, Scikit-learn  
- Development: Google Colab  
- Dataset: Self-captured images stored in `data/raw/`  

**7. RESULTS & DISCUSSION**

Example output:

| Fruit Image | Ripe % | Overripe % |
|------------|-------|------------|
| Banana Green | 89.74 | 10.26 |
| Banana Ripe | 69.68 | 30.32 |
| Banana Overripe | 63.47 | 36.53 |
| Apple Raw | 44.16 | 55.84 |
| Apple Red | 34.05 | 65.95 |
| Apple Ripe | 30.54 | 69.46 |

**Interpretation:**  
Ripeness decreases and over-ripeness increases → consistent with real fruit lifecycle.

**8. CONCLUSION**
A simple HSV-based segmentation technique with K-Means clustering successfully estimates fruit ripeness. The approach is low-cost, lightweight, and suitable for real-time quality inspection.

**9. FUTURE WORK**
- High-accuracy deep learning segmentation
- Larger and more diverse dataset
- Deployment on mobile devices or sorting machines
-
- **10. REFERENCES**
1️⃣OpenCV Documentation  
2️⃣ Scikit-learn KMeans Documentation  
3️⃣ Fruit Quality Analysis Studies



---
