<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Image Forgery Detection Project</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: #f7f9fc;
      color: #333;
      line-height: 1.6;
      margin: 0;
      padding: 0;
    }
    header {
      background-color: #0d1117;
      color: white;
      padding: 30px 20px;
      text-align: center;
    }
    h1, h2, h3 {
      color: #0d1117;
    }
    .container {
      max-width: 1000px;
      margin: 30px auto;
      padding: 20px;
      background: white;
      border-radius: 12px;
      box-shadow: 0 6px 20px rgba(0,0,0,0.1);
    }
    table {
      width: 100%;
      border-collapse: collapse;
      margin: 15px 0;
    }
    table, th, td {
      border: 1px solid #ddd;
    }
    th, td {
      padding: 12px;
      text-align: left;
    }
    th {
      background-color: #0d1117;
      color: white;
    }
    ul, ol {
      padding-left: 20px;
    }
    code {
      background-color: #eaeaea;
      padding: 2px 6px;
      border-radius: 5px;
      font-family: monospace;
    }
    pre {
      background-color: #eaeaea;
      padding: 15px;
      border-radius: 8px;
      overflow-x: auto;
    }
    footer {
      text-align: center;
      padding: 15px;
      margin-top: 30px;
      background-color: #0d1117;
      color: white;
      border-top-left-radius: 12px;
      border-top-right-radius: 12px;
    }
    a {
      color: #0366d6;
      text-decoration: none;
    }
    a:hover {
      text-decoration: underline;
    }
  </style>
</head>
<body>

<header>
  <h1>Image Forgery Detection Project</h1>
  <p>Hybrid SWT + CNN Model for Copy-Move and Splicing Forgery Detection</p>
</header>

<div class="container">

<h2>1. Description</h2>
<p>This project focuses on detecting <b>copy-move</b> and <b>splicing</b> forgeries in images using a <b>hybrid deep learning approach</b>.  
It combines <b>Stationary Wavelet Transform (SWT)</b> with a custom <b>CNN</b> to enhance feature extraction and improve detection accuracy.</p>
<ul>
  <li>Supports both copy-move and splicing forgery detection.</li>
  <li>Robust to noise, JPEG compression, rotation, and scaling.</li>
  <li>Lightweight CNN architecture with high accuracy.</li>
</ul>

<h2>2. Datasets Used</h2>
<table>
  <thead>
    <tr>
      <th>Forgery Type</th>
      <th>Dataset</th>
      <th>Link / DOI</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Copy-Move</td>
      <td>GRIP</td>
      <td><a href="https://github.com/greatzh/Image-Forgery-Datasets-List#GRIP" target="_blank">Link</a></td>
    </tr>
    <tr>
      <td>Copy-Move</td>
      <td>COVERAGE</td>
      <td><a href="https://github.com/greatzh/Image-Forgery-Datasets-List#COVERAGE" target="_blank">Link</a></td>
    </tr>
    <tr>
      <td>Copy-Move</td>
      <td>MICC-F2000</td>
      <td><a href="https://www.kaggle.com/datasets/manas29/micc-f2000" target="_blank">Kaggle Link</a></td>
    </tr>
    <tr>
      <td>Copy-Move</td>
      <td>MICC-F200</td>
      <td><a href="https://www.kaggle.com/datasets/nishaahin/miccf200" target="_blank">Kaggle Link</a></td>
    </tr>
    <tr>
      <td>Copy-Move</td>
      <td>CASIA-CMFD</td>
      <td><a href="https://www.kaggle.com/datasets/mashraffarouk/casia-cmfd" target="_blank">Kaggle Link</a></td>
    </tr>
    <tr>
      <td>Splicing</td>
      <td>CASIA V1</td>
      <td><a href="https://www.kaggle.com/datasets/sophatvathana/casia-dataset" target="_blank">Kaggle Link</a></td>
    </tr>
    <tr>
      <td>Splicing</td>
      <td>CASIA V2</td>
      <td><a href="https://www.kaggle.com/datasets/divg07/casia-20-image-tampering-detection-dataset" target="_blank">Kaggle Link</a></td>
    </tr>
  </tbody>
</table>

<h2>3. Code Information</h2>
<p>Implemented in Python 3 with TensorFlow/Keras and OpenCV.</p>
<pre>
/data           -> Datasets
/notebooks      -> Colab notebooks
/src            -> Model training and evaluation scripts
/results        -> Generated results (metrics, confusion matrices)
/README.html    -> This file
</pre>

<h2>4. Usage Instructions</h2>
<pre>
git clone https://github.com/drmahmoudatef/SWT-CNN-Model.git
cd SWT-CNN-Model
pip install -r requirements.txt
python src/train_model.py
python src/evaluate_model.py
</pre>
<p>View results in <code>/results</code> folder.</p>

<h2>5. Requirements</h2>
<ul>
  <li>Python 3.8+</li>
  <li>TensorFlow >= 2.9</li>
  <li>Keras >= 2.9</li>
  <li>OpenCV >= 4.5</li>
  <li>NumPy, Pandas</li>
  <li>Matplotlib, Seaborn</li>
  <li>PyWavelets</li>
  <li>Pillow</li>
  <li>scikit-learn</li>
  <li>scikit-image</li>
</ul>

<h2>6. Methodology</h2>
<ol>
  <li>Image Preprocessing: Resize, normalize, and augment images.</li>
  <li>SWT Decomposition: Decompose images into four sub-bands (LL, LH, HL, HH).</li>
  <li>Feature Fusion: Combine sub-bands into a 4-channel input for CNN.</li>
  <li>CNN Training: Train on multiple datasets with data augmentation.</li>
  <li>Evaluation: Compute Accuracy, Precision, Recall, F1-score, Confusion matrices.</li>
  <li>Comparative Analysis: Compare with baseline CNN and traditional methods.</li>
  <li>Robustness Testing: Evaluate performance under noise, compression, rotation, scaling.</li>
</ol>

<h2>7. Results</h2>
<ul>
  <li>Accuracy: 97–100% across datasets.</li>
  <li>High Precision, Recall, and F1-score.</li>
  <li>Robust under post-processing attacks.</li>
</ul>

<h2>8. Conclusions & Limitations</h2>
<p><b>Conclusions:</b> SWT + CNN hybrid model achieves high detection performance across multiple datasets.</p>
<p><b>Limitations:</b> Requires GPU for large datasets, dataset imbalance may affect minority class, unseen manipulation types reduce accuracy.</p>

<h2>9. Citations</h2>
<pre>
@article{Atef2025SWT_CNN,
  title={Image Forgery Detection Using SWT + CNN Hybrid Model},
  author={Mahmoud Atef},
  journal={Journal of Computer Vision Research},
  year={2025}
}
</pre>

<h2>10. License & Contribution</h2>
<p>MIT License. Contributions welcome via pull requests.</p>

<h2>11. Connect with Me</h2>
<p>
  <a href="https://github.com/drmahmoudatef" target="_blank">GitHub</a> | 
  <a href="https://www.linkedin.com/in/drmahmoudatef" target="_blank">LinkedIn</a>
</p>

</div>

<footer>
  &copy; 2025 Mahmoud Atef | Image Forgery Detection Project
</footer>

</body>
</html>
