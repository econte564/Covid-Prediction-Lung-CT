# Covid-Prediction-Lung-CT
A simple framework to detect the Covid-19 by analyzing the lung scans CT.

<h2>Problem Description</h2>
The goal of this research is to train a classifier to recognize Covid-19 positive patients from their CT lungs scans in order to support the physician’s decision process with a quantitative approach.

<h2>Dataset</h2>
<ul>
<li> Original positive data: https://wiki.cancerimagingarchive.net/pages/viewpage.action?pageId=80969742 </li>
<li> Orifinal negative data: https://wiki.cancerimagingarchive.net/pages/viewpage.action?pageId=80969771#80969771bcab02c187174a288dbcbf95d26179e8 </li>
<li> Link to our custom dataset: https://drive.google.com/file/d/112rnDTasnEIYrHm6E2sd-EgNbi-UKuKV/view?usp=sharing </li>
</ul>

<h2>Pipeline</h2>
The general pipeline process is:
<p><ol>
<li> Slices Selection </li>
<li> Mask Generation </li>
<li> Mask Fill </li>
<li> Histogram Equalization and Filtering </li>
<li> Haralick Features Extraction </li>
<li> Feature Reshaping </li>
<li> Feature Reduction through PCA </li>
<li> Feeding to the Classifier </li>
</ol></p>

![Pipeline image](https://github.com/MattiaRigi97/Covid-Prediction-Lung-CT/blob/main/images/pipeline.jpg?raw=true)

<h2>Features extraction and PCA</h2>
We obtain three 4x13 matrices that we reshape into a single vector of 156 features. We first attempt to perform feature selection by eliminating the least contributing features. However, the loss of information is excessive. So, given the high dimensionality, we opt for a feature synthesis approach and apply PCA to only retain the first 2 Principal Components as they alone explain ~89% of the total variability.

<h2>Model</h2>
Finally, the processed data is fed into the different Classifiers (SVM, Logistic Regression, Random Forest, Ensemble methods). All methods were tested with 5-fold Cross Validation and 80/20 train/test split stratified on the labels. SVM with a linear kernel obtained the best results both in terms of AUC(85%), Accuracy(81%), Precision (81%) and Recall(80%). The counfusion matrix and the AUC plot is reported below: <br />

<br />

<center>

![Confusion matrix](https://github.com/MattiaRigi97/Covid-Prediction-Lung-CT/blob/main/images/confusion_matrix.jpg?raw=true) 

</center>


![AUC](https://github.com/MattiaRigi97/Covid-Prediction-Lung-CT/blob/main/images/AUC.jpg?raw=true)
