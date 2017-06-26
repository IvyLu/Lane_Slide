## Self-Driving Car  
## Lane Recognition

### Ivy Lu

---

### Introduction

- Identify Lane in Images
- *Python* and *OpenCV* Packages


![original](images/0original.jpg)
![final](images/6final.jpg)

---

### Step 1: Turn Image to Grayscale

![grayscale](images/1grayscale.png)

- Reduce complexity
- color doesn't help much in solving this problem

---

### Step 2: Gaussian Smoothing

![gaussian](images/2kernel.png)

- Suppressing noise, reduce details
- Low-pass filter, reduce high-frequency components
- Convolving image with Gaussian function

---
 
### Step 3: Canny Edge Detection

![canny](images/3gradient.png)

- **Low error rate**: good detection of only existent edges
- **Good localization**: close to real edge pixels 
- **Minimal response**: only one response per edge

---

### Step 4: Create Mask 

![mask](images/4mask.png)

- Assumption: fixed camera


![masked](images/4masked.png)

---

### Step 5: Hough Transform

![parameterspace](images/5houghspace.png)

**y = mx + b**    =>    **b = -xm + y**

Find points in Hough space where multiple lines cross

![parameter](images/5houghparameter.png)


![hough](images/5houghline.png) ![overlap](images/5overlap.png)

---

### Step 6: Draw Line

![final](images/6final.jpg)

- Connect, Average, Extrapolate

