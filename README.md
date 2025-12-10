<h1><img src="https://emojis.slackmojis.com/emojis/images/1531849430/4246/blob-sunglasses.gif?1531849430" width="30"/> Deep Image Forgery Detection</h1>

<p>Welcome to the repository for my research on <b>Copy-Move and Splicing Forgery Detection</b> using a hybrid deep learning approach. </br>
This project integrates the <b>Stationary Wavelet Transform (SWT)</b> with a custom <b>Deep Convolutional Neural Network (DCNN)</b> to detect image manipulations with high accuracy and robustness.</p>

<h3>📄 Abstract</h3>
<p>
Copy-move and splicing forgery are common methods of image manipulation. This study proposes a hybrid model combining <b>SWT</b> and <b>DCNN</b> to enhance forgery detection. 
The SWT decomposes images into four frequency sub-bands (LL, LH, HL, HH), preserving spatial information critical for detecting forgery patterns. 
These features are then merged into a single augmented image and fed into a CNN for improved classification.
The model was evaluated on seven benchmark datasets: 
<b>GRIP, COVERAGE, MICC-F220, MICC-F2000, CASIA-CMFD</b> (copy-move forgery), and <b>CASIA V1, CASIA V2</b> (splicing forgery).
The experimental results showed exceptional performance, with 100% precision, recall, F1-score, and accuracy across most datasets, 
and 97% accuracy for GRIP. Robustness tests against Gaussian noise, JPEG compression, rotation, and scaling yielded 96–97% accuracy, demonstrating high generalization and reliability.
</p>

<h3>Datasets</h3>
<ul>
  <li><b>Copy-Move Forgery:</b> GRIP, COVERAGE, MICC-F220, MICC-F2000, CASIA-CMFD</li>
  <li><b>Splicing Forgery:</b> CASIA V1, CASIA V2</li>
</ul>

<h3>Methodology</h3>
<ul>
  <li>Apply <b>Stationary Wavelet Transform (SWT)</b> to decompose images into LL, LH, HL, HH sub-bands.</li>
  <li>Combine the sub-bands into a 4-channel image as input to a custom CNN.</li>
  <li>Train the model on multiple datasets for 15 epochs, using data augmentation and class weighting.</li>
  <li>Evaluate model performance using accuracy, precision, recall, F1-score, and confusion matrices.</li>
</ul>

<h3>Key Results</h3>
<ul>
  <li>Accuracy: 97–100% across seven datasets.</li>
  <li>Robustness to Gaussian noise, JPEG compression, rotation, and scaling.</li>
  <li>Demonstrated strong generalization and detection of subtle manipulations.</li>
</ul>

<h3>Things I work with</h3>
<p>
  <img alt="Python" src="https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white" />
  <img alt="TensorFlow" src="https://img.shields.io/badge/-TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white" />
  <img alt="Keras" src="https://img.shields.io/badge/-Keras-D00000?style=flat-square&logo=keras&logoColor=white" />
  <img alt="PyTorch" src="https://img.shields.io/badge/-PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" />
  <img alt="OpenCV" src="https://img.shields.io/badge/-OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white" />
  <img alt="NumPy" src="https://img.shields.io/badge/-NumPy-013243?style=flat-square&logo=numpy&logoColor=white" />
</p>

<h3>Featured Projects</h3>
<table>
  <thead align="center">
    <tr>
      <td><b>Project</b></td>
      <td><b>Datasets</b></td>
      <td><b>Accuracy</b></td>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><b>Hybrid CNN + SWT for Copy-Move & Splicing Detection</b></td>
      <td>GRIP, COVERAGE, MICC-F220, MICC-F2000, CASIA-CMFD, CASIA V1, CASIA V2</td>
      <td>97–100%</td>
    </tr>
  </tbody>
</table>

<h3>Where to find me</h3>
<p>
  <a href="#" target="_blank"><img alt="GitHub" src="https://img.shields.io/badge/GitHub-%2312100E.svg?&style=for-the-badge&logo=Github&logoColor=white" /></a>
  <a href="#" target="_blank"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white" /></a>
</p>

<hr/>

<p align="center">This <i>README</i> highlights the research on image forgery detection using hybrid deep learning models. It is designed to provide clarity, professionalism, and a quick overview for collaborators and readers.</p>
