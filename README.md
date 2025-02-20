#  Classification Using Unsupervised Learning

## Introduction

Echo classification is a crucial task in remote sensing and environmental monitoring. By analyzing satellite echoes, we can distinguish between open water leads and ice-covered areas, which is vital for understanding sea ice dynamics, climate change, and navigation safety in polar regions. This project applies unsupervised learning techniques to classify echoes into **leads** and **sea ice**, providing statistical insights and model evaluation.

## **Overview**  

This notebook explores **unsupervised learning methods** for classifying sea ice and leads using **remote sensing data** from Sentinel-2 (optical imagery) and Sentinel-3 (altimetry data). Unsupervised learning is valuable in Earth Observation (EO) applications where labeled data is limited or unavailable.  

We implement **two clustering techniques** to differentiate between sea ice and leads:  
1. **K-Means Clustering** – A simple and efficient algorithm that assigns each data point to the nearest cluster centroid.  
2. **Gaussian Mixture Models (GMM)** – A probabilistic clustering method that captures more nuanced variations in the data.  

The notebook follows these key steps:  

1. **Data Preprocessing:**  
   - Loading Sentinel-2 optical bands and Sentinel-3 altimetry data.  
   - Extracting relevant features, including **peakiness and stack standard deviation (SSD)** from altimetry waveforms.  
   - Standardizing data for clustering analysis.  

2. **Clustering & Classification:**  
   - Applying **K-Means and GMM** to segment Sentinel-2 optical data into two classes: **sea ice and leads**.  
   - Using **GMM clustering** to classify Sentinel-3 altimetry waveforms based on extracted features.  

3. **Statistical Analysis:**  
   - Computing the **average waveform shape** and **standard deviation** for classified echoes.  
   - Comparing the variability between sea ice and leads to validate classification accuracy.  

4. **Model Evaluation:**  
   - **Confusion matrix analysis**: Comparing the clustering results against the official **ESA classification dataset**.  
   - Evaluating **precision, recall, and overall accuracy** to assess model performance.  

### **Ultimate Goal**  
The primary objective of this notebook is to **quantify echo classification performance** by:  
✅ Classifying **sea ice vs. leads** using clustering techniques.  
✅ Computing **average waveform properties** for each class.  
✅ Comparing results against **ESA's official classification** using a confusion matrix.  



## File in This Repository
- `Unsupervised_Learning_Methods.ipynb` - The main notebook containing the code and results.

## Requirements
To run this notebook, you need the following libraries:

```bash
pip install pandas numpy sklearn matplotlib seaborn
```

## How to Use This Notebook
1. **Open in Google Colab**: You can open this notebook in Google Colab by uploading it to your Google Drive and accessing it via Colab.
2. **Run the Code**: Execute the cells in order to perform classification and evaluation.
3. **Modify if Needed**: Adjust parameters for clustering or classification based on your dataset.

## Steps Performed in This Notebook
1. **Data Loading** - Reads the dataset from Google Drive by mounting it.
2. **Echo Classification** - Uses clustering (K-Means) to classify echoes into leads and sea ice.
3. **Statistical Analysis** - Computes average echo shape and standard deviation.
4. **Confusion Matrix** - Compares the results with ESA's official classification.
5. **Visualization** - Plots echo distributions and classification results.


## Expected Results

After running the notebook, you should see the following key results:

1. **Average Echo Shape & Standard Deviation**  
   - To better understand the characteristics of each classified group, we compute the **average echo shape** and **standard deviation** for both **leads** and **sea ice**.  
   - These statistical insights help quantify differences in reflectance properties between the two categories.  

2. **Clustered Echo Classification (K-Means & GMM)**  
   - The final clustering results show how our unsupervised learning techniques categorize echoes into **leads** and **sea ice**.  
   - A scatter plot of the clustered data provides a visual confirmation that our method successfully differentiates between the two classes.  

3. **Confusion Matrix**  
   - The confusion matrix provides a direct comparison between our classification and ESA's official labels.  
   - It helps measure **accuracy and misclassification rates**, ensuring that our model aligns well with real-world data.  


## References

Below are the references used in this project:

- Bishop, C. M. (2006). *Pattern Recognition and Machine Learning*. Springer.
- MacQueen, J. (1967). Some methods for classification and analysis of multivariate observations. In *Proceedings of the Fifth Berkeley Symposium on Mathematical Statistics and Probability* (Vol. 1, pp. 281-297).
- Reynolds, D. A. (2009). Gaussian Mixture Models. In *Encyclopedia of Biometrics* (pp. 659-663). Springer.
- McLachlan, G., & Peel, D. (2004). *Finite Mixture Models*. Wiley-Interscience.
- ESA Data Documentation: [https://earth.esa.int/eogateway/](https://earth.esa.int/eogateway/)
- Scikit-Learn Documentation: [https://scikit-learn.org/stable/](https://scikit-learn.org/stable/)
- Matplotlib Documentation: [https://matplotlib.org/stable/](https://matplotlib.org/stable/)


## Contact

For any questions, feel free to reach out!

📧 **UCL Email:** hamzah.rahman.22@ucl.ac.uk


