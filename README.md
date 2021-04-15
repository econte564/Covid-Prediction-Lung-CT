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
<ol>
<li> Slices Selection </li>
<li> Mask Generation </li>
<li> Mask Fill </li>
<li> Histogram Equalization and Filtering </li>
<li> Haralick Features Extraction </li>
<li> Feature Reshaping </li>
<li> Feature Reduction through PCA </li>
<li> Feeding to the Classifier </li>
</ol>

![Pipeline image](https://github.com/MattiaRigi97/Covid-Prediction-Lung-CT/blob/main/images/pipeline.jpg?raw=true)

<p>ciao<\p>
