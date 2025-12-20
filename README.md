<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Image Forgery Detection using SWT and CNN</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
body {
    font-family: Arial, Helvetica, sans-serif;
    background-color: #f7f9fc;
    color: #222;
    line-height: 1.7;
    margin: 0;
    padding: 0;
}

header {
    background-color: #0d1117;
    color: #ffffff;
    padding: 40px 20px;
    text-align: center;
}

.container {
    max-width: 1100px;
    margin: 30px auto;
    padding: 25px;
    background: #ffffff;
    border-radius: 10px;
    box-shadow: 0 5px 18px rgba(0,0,0,0.1);
}

h1, h2, h3 {
    color: #0d1117;
}

table {
    width: 100%;
    border-collapse: collapse;
    margin: 20px 0;
}

table, th, td {
    border: 1px solid #ccc;
}

th, td {
    padding: 12px;
    text-align: left;
}

th {
    background-color: #0d1117;
    color: #ffffff;
}

code {
    background-color: #eeeeee;
    padding: 3px 6px;
    border-radius: 4px;
    font-family: Consolas, monospace;
}

pre {
    background-color: #eeeeee;
    padding: 15px;
    border-radius: 6px;
    overflow-x: auto;
}

footer {
    background-color: #0d1117;
    color: white;
    text-align: center;
    padding: 15px;
    margin-top: 40px;
}
</style>
</head>

<body>

<header>
<h1>Image Forgery Detection Using SWT + CNN</h1>
<p>Hybrid Deep Learning Framework for Copy-Move and Splicing Forgery Detection</p>
</header>

<div class="container">

<h2>1. Project Overview</h2>
<p>
This project presents a robust hybrid deep learning framework for 
<strong>image forgery detection</strong>, targeting both 
<strong>copy-move</strong> and <strong>splicing</strong> manipulations.
The proposed approach integrates <strong>Stationary Wavelet Transform (SWT)</strong>
with a custom-designed <strong>Convolutional Neural Network (CNN)</strong>
to enhance discriminative feature extraction and improve detection accuracy.
</p>

<h2>2. Key Contributions</h2>
<ul>
<li>Integration of SWT with CNN to capture spatial and frequency-domain artifacts.</li>
<li>Custom lightweight CNN architecture with high detection accuracy.</li>
<li>Robust evaluation under class imbalance using class weighting.</li>
<li>Extensive evaluation using multiple forensic performance metrics.</li>
</ul>

<h2>3. Datasets</h2>
<table>
<thead>
<tr>
<th>Forgery Type</th>
<th>Dataset</th>
<th>Source</th>
</tr>
</thead>
<tbody>
<tr>
<td>Copy-Move</td>
<td>MICC-F2000</td>
<td>https://www.kaggle.com/datasets/manas29/micc-f2000</td>
</tr>
<tr>
<td>Copy-Move</td>
<td>MICC-F200</td>
<td>https://www.kaggle.com/datasets/nishaahin/miccf200</td>
</tr>
<tr>
<td>Splicing</td>
<td>CASIA V2</td>
<td>https://www.kaggle.com/datasets/divg07/casia-20-image-tampering-detection-dataset</td>
</tr>
<tr>
<td>Splicing</td>
<td>CASIA V1</td>
<td>https://www.kaggle.com/datasets/sophatvathana/casia-dataset</td>
</tr>
<tr>
<td>Copy-Move</td>
<td>CASIA-CMFD</td>
<td>https://www.kaggle.com/datasets/mashraffarouk/casia-cmfd</td>
</tr>
</tbody>
</table>

<p>
All datasets were downloaded from Kaggle, reorganized, and split into 
<strong>training</strong>, <strong>validation</strong>, and <strong>testing</strong>
sets on Google Drive, then accessed via Google Colab.
</p>

<h2>4. Methodology</h2>
<ol>
<li><strong>Preprocessing:</strong> Image resizing to 224×224 and normalization.</li>
<li><strong>SWT Decomposition:</strong> Haar wavelet used to extract LL, LH, HL, HH sub-bands.</li>
<li><strong>Feature Fusion:</strong> Four sub-bands stacked into a 4-channel input tensor.</li>
<li><strong>CNN Architecture:</strong> Three convolutional blocks followed by GAP and dense layers.</li>
<li><strong>Training:</strong> Binary cross-entropy loss with Adam optimizer.</li>
<li><strong>Class Imbalance Handling:</strong> Class weights computed dynamically.</li>
</ol>

<h2>5. Model Architecture Summary</h2>
<pre>
Input: 224 × 224 × 4 (SWT channels)
Conv Blocks: 32 → 64 → 128 filters
Batch Normalization after each convolution
Global Average Pooling
Dense (512) + Dropout (0.5)
Output: Sigmoid (Binary Classification)
</pre>

<h2>6. Training Configuration</h2>
<ul>
<li>Optimizer: Adam</li>
<li>Learning Rate: 0.001</li>
<li>Loss Function: Binary Cross-Entropy</li>
<li>Batch Size: 32</li>
<li>Epochs: 15</li>
<li>Callbacks: ModelCheckpoint, CSVLogger</li>
</ul>

<h2>7. Evaluation Metrics</h2>
<p>
The model performance was evaluated using a comprehensive set of forensic metrics:
</p>
<ul>
<li>Accuracy</li>
<li>Precision</li>
<li>Recall (TPR)</li>
<li>True Negative Rate (TNR)</li>
<li>False Positive Rate (FPR)</li>
<li>False Negative Rate (FNR)</li>
<li>F1-Score</li>
<li>Matthews Correlation Coefficient (MCC)</li>
<li>Confusion Matrix Analysis</li>
</ul>

<h2>8. Experimental Results</h2>
<p>
Experimental results demonstrate that the proposed SWT + CNN framework achieves
<strong>high detection accuracy</strong> across multiple datasets and maintains
robust performance under various forgery scenarios.
</p>

<h2>9. Limitations</h2>
<ul>
<li>Computational cost increases with large datasets.</li>
<li>Requires GPU acceleration for efficient training.</li>
<li>Performance may degrade on unseen manipulation types.</li>
</ul>

<h2>10. Conclusion</h2>
<p>
This work confirms that combining Stationary Wavelet Transform with deep CNN
architectures significantly enhances image forgery detection performance,
making the proposed framework suitable for real-world digital forensic applications.
</p>

<h2>11. Author</h2>
<p>
<strong>Mahmoud Atef</strong><br>
PhD Researcher – Image Forensics & Deep Learning
</p>

</div>

<footer>
&copy; 2025 Mahmoud Atef – Image Forgery Detection using SWT and CNN
</footer>

</body>
</html>
