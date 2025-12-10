<h1><img src="https://emojis.slackmojis.com/emojis/images/1531849430/4246/blob-sunglasses.gif?1531849430" width="30"/> Image Forgery Detection Project</h1>

<p>Welcome to this repository! This project focuses on detecting <b>copy-move</b> and <b>splicing</b> forgeries in images using a hybrid deep learning approach. 
We combine the <b>Stationary Wavelet Transform (SWT)</b> with a custom <b>CNN model</b> to enhance feature extraction and improve detection accuracy.</p>

<h3>Datasets Used</h3>
<ul>
  <li><b>Copy-Move Forgery:</b> GRIP, COVERAGE, MICC-F220, MICC-F2000, CASIA-CMFD</li>
  <li><b>Splicing Forgery:</b> CASIA V1, CASIA V2</li>
</ul>

<h3>Method Overview</h3>
<ul>
  <li>Apply <b>SWT</b> to decompose images into four frequency sub-bands (LL, LH, HL, HH).</li>
  <li>Combine sub-bands into a 4-channel image as input for the CNN.</li>
  <li>Train the model using multiple datasets with data augmentation.</li>
  <li>Evaluate performance using accuracy, precision, recall, F1-score, and confusion matrices.</li>
</ul>

<h3>Key Features</h3>
<ul>
  <li>High detection accuracy across seven datasets.</li>
  <li>Robust against noise, JPEG compression, rotation, and scaling.</li>
  <li>Supports both copy-move and splicing forgery detection.</li>
  <li>Uses a lightweight CNN with enhanced feature extraction from SWT.</li>
</ul>

<h3>Tools & Technologies</h3>
<p>
  <img alt="Python" src="https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white" />
  <img alt="TensorFlow" src="https://img.shields.io/badge/-TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white" />
  <img alt="Keras" src="https://img.shields.io/badge/-Keras-D00000?style=flat-square&logo=keras&logoColor=white" />
  <img alt="OpenCV" src="https://img.shields.io/badge/-OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white" />
  <img alt="NumPy" src="https://img.shields.io/badge/-NumPy-013243?style=flat-square&logo=numpy&logoColor=white" />
</p>

<h3>Results</h3>
<ul>
  <li>Accuracy: 97–100% across the datasets.</li>
  <li>High precision, recall, and F1-score.</li>
  <li>Robust performance under post-processing attacks like noise and compression.</li>
</ul>

<h3>Connect with Me</h3>
<p>
  <a href="#" target="_blank"><img alt="GitHub" src="https://img.shields.io/badge/GitHub-%2312100E.svg?&style=for-the-badge&logo=Github&logoColor=white" /></a>
  <a href="#" target="_blank"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white" /></a>
</p>

<hr/>

<p align="center">This README summarizes the image forgery detection project using a hybrid SWT + CNN approach.</p>
