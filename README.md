# Data Visualization Projects
---


This repository contains detailed explanations about different approaches that I have used in Data Visualization problems. 

<u>Table of contents</u>
=======

<!--ts-->
  - [Project 1 - Intoxication Behavior](#project-1---intoxication-behavior)
      - [Problem Statement ](#problem-statement-1)
  - [Project 2 - Dimension Reduction](#project-2---dimension-reduction)
      - [Problem Statement](#problem-statement-2)
      - [Data Analysis & Preprocessing](#project2-2)
      - [Visualization](#visualization2)
<!--te-->

---

## Project 1 - Intoxication Behavior
#### Problem Statement <a id="problem-statement-1"></a>
Content for Problem Statement 1 goes here.



---
## Project 2 - Dimension Reduction

#### Problem Statement <a id="problem-statement-2"></a>
The dataset provides valuable insights into breast cancer diagnoses, with a focus on various attributes related to tumor characteristics. The main goal of this project is to detect hidden patterns between various attributes within the dataset by utilizing data visualization methods.

#### Data Analysis & Preprocessing <a id="project2-2"></a>
The dataset includes 569 samples with 32 dimensions, comprising patient IDs, diagnosis status, and 30 tumor-related features. The dataset can be divided into three subsets, each consisting of 10 features:

<div style="display: flex; justify-content: center; align-items: center; text-align: center;">
  <img src="./Images/Project2/2-1.png" alt="Image 2-1" width=300 style="margin: 0 10px;">
  <img src="./Images/Project2/2-2.png" alt="Image 2-2" width=360 style="margin: 0 10px;">
</div>



<br><br>
Tumor Geometry
- Radius: Mean distance from center to perimeter points
- Texture: Standard deviation of gray-scale values
- Perimeter: Perimeter measurement
- Area: Area measurement
<br>

Tumor Smoothness
- Smoothness: Local variation in radius lengths
- Compactness: Computed as (perimeter^2) / area - 1.0
- Concavity: Severity of concave portions of the contour
- Concave Points: Number of concave portions of the contour
<br>

Tumor Symmetry
- Symmetry: Symmetry of tumor
- Fractal Dimension: Fractal dimension of tumor
 <br>

<!-- ![hey](./test.jpg) -->

To effectively utilize this dataset for visualization and future modeling, it's essential to ensure that all variables are in numeric format. The dataset primarily comprises numeric attributes, with one exception: the "Diagnosis" column. It contains two parameters: <br>
- "Malignant" cases indicate tumors that are potentially dangerous and have spread significantly.
- "Benign" cases refer to tumors that are less dangerous and have not spread extensively.

To prepare the dataset for analysis, we will convert the "Diagnosis" variable into a numeric format, enabling us to employ various visualization techniques and modeling approaches effectively.

#### Visualization  <a id="visualization2"></a>
After preprocessing phase, let's start with visualization and utilizing various visualization techniques to gather more concise understanding.

<div style="display: flex; justify-content: center; align-items: center; text-align: center;">
  <img src="./Images/Project2/2-3.png" alt="Image 2-1" width=540 style="margin: 0 10px;">
</div>

<br>

Next, the analysis involves visualizing the remaining 30 features to explore their relationships. histogram visualizations are provided for the mean, standard error (SE), and worst-case features. These visualizations offer a clear view of each variable's behavior.

<div style="text-align:center;">
  <img src="./Images/Project2/2-4.png" alt="Image 2-1" width=500 style="display:inline-block; margin:0 2px;">
</div>

<div style="text-align:center;">
  <img src="./Images/Project2/2-5.png" alt="Image 2-2" width=500 style="display:inline-block; margin:0 10px;">
</div>

<div style="text-align:center;">
  <img src="./Images/Project2/2-6.png" alt="Image 2-1" width=500 style="display:inline-block; margin:0 2px;">
</div>

<br>

Also, density plots were employed to provide a visual representation. These plots effectively reveal exponential behavior within various variables. For instance, the plots clearly indicate that the variables "area," "compactness," and "fractal_dimension" exhibit exponential distributions.

<div style="text-align:center;">
  <img src="./Images/Project2/2-7.png" alt="Image 2-1" width=500 style="display:inline-block; margin:0 2px;">
</div>

<div style="text-align:center;">
  <img src="./Images/Project2/2-8.png" alt="Image 2-2" width=500 style="display:inline-block; margin:0 10px;">
</div>

<div style="text-align:center;">
  <img src="./Images/Project2/2-9.png" alt="Image 2-1" width=500 style="display:inline-block; margin:0 2px;">
</div>

<br>

At this stage, sufficient knowledge about the dataset has been acquired, enabling us to proceed with the visualization of a heatmap. There is a potential usage of heatmap for dimension reduction to observe the correlations between all features of the dataset.

<div style="text-align:center;">
  <img src="./Images/Project2/2-10.png" alt="Image 2-1" width=600 style="display:inline-block; margin:0 2px;">
</div>

<br>

In the pursuit of feature selection, a comprehensive comparison was conducted among the subsets (mean, SE, and worst). Notably, correlations emerged within these subsets.
This process continued iteratively until no fully correlated features, characterized by a correlation coefficient of 1, remained in the heatmap. 

<div style="text-align:center;">
  <img src="./Images/Project2/2-11.png" alt="Image 2-1" width=600 style="display:inline-block; margin:0 2px;">
</div>