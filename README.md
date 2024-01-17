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
 <h1>Training Overview</h1>
<p>The training process covered 25 epochs, monitoring the model's performance through Loss and Intersection over Union (IoU) metrics for both training and validation datasets. The journey from the initial to the final epoch highlights the model's learning progression and adaptation to the complexities of the dataset.</p>

<h2>Initial Phase (Epochs 1-5)</h2>
<p>The training commenced with a relatively high loss, which progressively decreased, indicating the model's initial adaptation and learning from the data. The validation IoU showed a gradual increase, reflecting the model's improving capability in segmenting the images accurately.</p>

<h2>Mid-Training Phase (Epochs 6-15)</h2>
<p>During this phase, the model's performance demonstrated consistent improvement, with both training and validation losses decreasing. This period marked the model's capability to refine its predictions and capture more subtle features of the dataset. A notable drop in Val Loss and a rise in Val IoU during Epochs 15 and 16 signify a significant leap in the model's validation performance.</p>

<h2>Late Training Phase (Epochs 16-25)</h2>
<p>The concluding stages of the training showed the model's continued refinement with a general trend of decreasing loss and improving IoU. Epochs 22 to 25 marked the highest validation IoUs, indicating the model's strong performance in generalizing to unseen data. However, a slight increase in validation loss towards the end suggests the possibility of minor overfitting or inconsistencies in the validation dataset.</p>

  <h3>Epoch vs Loss Graph:</h3>
  <img src="https://github.com/avintech/monuseg-challenge/assets/64296499/e615d651-a3cb-45bd-a13c-987e3fbb1d23">
<p>Throughout the training epochs, the model demonstrated a steady improvement in its ability to segment images, as evidenced by the decreasing trend in loss and the increasing trend in IoU. The training process revealed the model's capability to learn and adapt to the dataset's intricacies. However, the slight fluctuations in validation metrics towards the end highlight the need for careful observation and potential adjustments in the model or data processing pipeline to ensure robustness and reliability in the model's predictions.</p>

  <h2>Validation Phase</h2>
  <h3>Evaluation Results:</h3>
    <ul>
      <li><code>Average IoU on Validation Set: 0.6200</code></li>
      <li><code>Average Precision: 0.7228</code></li>
      <li><code>Average Recall: 0.8264</code></li>
      <li><code>Average F1 Score: 0.7712</code></li>
  </ul>
  <h2>Conclusion</h2>
  <p>The evaluation results showcase the effectiveness of the U-Net model in image segmentation tasks. The balanced performance across precision, recall, and IoU underscores the model's capability in identifying and delineating relevant segments accurately, making it a robust tool for image segmentation applications, particularly in medical imaging.</p>

</div>
