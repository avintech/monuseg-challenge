# Project Overview
This project is done as part of the Computer Vision Module in SIT where we are supposed to attempt the MoNuSeg challenge.

The MoNuSeg (Multi-Organ Nucleus Segmentation) Challenge is a scientific competition focused on the task of segmenting nuclei in histopathology images. Histopathology, the study of changes in tissues due to disease, often involves examining thin slices of tissue under a microscope. Nuclei segmentation is a crucial step in this process, as it helps in identifying and analyzing cellular structures within these tissues.

<div>
  <h2>Model Overview</h2>
  <p>We decided to use the U-Net model as it is a deep learning model that excels in the task of segmenting images into multiple classes. It is especially well-suited for medical image segmentation tasks. The model is built using the PyTorch framework.</p>
  <h2>Architecture</h2>
  <p>The architecture of the U-Net model is symmetric, with a contracting path to capture context and an expansive path that enables precise localization. Key features include:</p>
  <ul>
      <li><strong>Contracting Path:</strong> Consists of repeated blocks of convolutional and max pooling layers for feature extraction and dimensionality reduction.</li>
      <li><strong>Expansive Path:</strong> Involves upsampling and concatenation with corresponding feature maps from the contracting path, aiding in precise localization.</li>
      <li><strong>Skip Connections:</strong> Provide shortcuts between layers of equal resolution in the contracting and expansive paths, helping in the preservation of fine details </li>
      <li><strong>Final Layer:</strong> A 1x1 convolution that maps the feature vectors to the desired number of segmentation classes.</li>
  </ul>
  <p>This is an example of what a U-Net model may look like:</p>
  <img src="https://github.com/avintech/monuseg-challenge/assets/64296499/e7d14708-2175-43a6-816e-359c67af72e6">
</div>
<div>
  <h2>Training Phase</h2>
  <h3>Epoch vs Loss Graph:</h3>
  <Insert Epoch vs Loss Graph & Description Here>
  
  <h2>Validation Phase</h2>
  <h3>Evaluation Results:</h3>
    <ul>
      <li><code>Average IoU on Validation Set: 0.6200</code></li>
      <li><code>Average Precision: 0.7684</code></li>
      <li><code>Average Recall: 0.7621</code></li>
      <li><code>Average F1 Score: 0.7650</code></li>
  </ul>
</div>
