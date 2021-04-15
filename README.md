# Covid-Prediction-Lung-CT
A simple framework to detect the Covid-19 by analyzing the lung scans CT.

<h2>Problem Description</h2>
The goal of this research is to train a classifier to recognize Covid-19 positive patients from their CT lungs scans in order to support the physician’s decision process with a quantitative approach.

<h2>Dataset</h2>
- Original positive data: https://wiki.cancerimagingarchive.net/pages/viewpage.action?pageId=80969742
- Orifinal negative data: https://wiki.cancerimagingarchive.net/pages/viewpage.action?pageId=80969771#80969771bcab02c187174a288dbcbf95d26179e8 
Link to our custom dataset: https://drive.google.com/file/d/112rnDTasnEIYrHm6E2sd-EgNbi-UKuKV/view?usp=sharing

<h2>Pipeline</h2>
The general pipeline process is:
- Slices Selection 
- Mask Generation
- Mask Fill
- Histogram Equalization and Filtering
- Haralick Features Extraction
- Feature Reshaping
- Feature Reduction through PCA
- Feeding to the Classifier


