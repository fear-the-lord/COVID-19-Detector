# COVID-19-Detector

<h2>PROBLEM STATEMENT</h2>
<p>Detection of COVID-19 presence from Chest X-ray scans using CNN & Class Activation Maps<p>
<hr style="width:50%;text-align:left;margin-left:0">
  
<h2>OVERVIEW</h2>
<p>The 2019–20 coronavirus pandemic is an ongoing pandemic of coronavirus disease 2019 (COVID-19) caused by severe acute respiratory syndrome coronavirus 2 <b>(SARS‑CoV‑2)</b>. The outbreak was identified in Wuhan, China, on November 17, 2019. The World Health Organization declared the outbreak a Public Health Emergency of International Concern on 30 January, and a pandemic on 11 March. As of 30 April 2020, more than 3.19 million cases of COVID-19 have been reported in 185 countries and territories, resulting in more than 227,000 deaths. More than 972,000 people have recovered.</p>

<p>Recommended preventive measures include hand washing, covering one's mouth when coughing, maintaining distance from other people, wearing a face mask in public settings, and monitoring and self-isolation for people who suspect they are infected. Authorities worldwide have responded by implementing travel restrictions, quarantines, curfews and stay-at-home orders, workplace hazard controls, and facility closures. Many places have also worked to increase testing capacity and trace contacts of infected persons.</p>

<p>So, one thing that is needed to be done in this case is Multiple Testing, so that the actual situation is correctly understood and proper preventive actions are taken. Another important thing is to bring out the test results quickly.</p>

<p>The standard COVID-19 tests are called <b>PCR (Polymerase chain reaction)</b> tests which look for the existence of antibodies of a given infection. But there are a few issues with the test. Pathogenic laboratory testing is the diagnostic gold standard but it is time-consuming with significant false-negative results. However, large scale implementation of the PCR tests are costly and cannot be implemented by some of the developing countries. So, to make things fast and cheap, we can use Deep Learning and Machine Learning concepts.</p>
<hr style="width:50%;text-align:left;margin-left:0">

<h2>THINGS TO DO</h2>
<p><ul>
  <li>Create the dataset.</li>
  <li>Import the necessary dependencies.</li>
  <li>Build the CNN Model.</li>
  <li>Pre-process the images.</li>
  <li>Train the model.</li>
  <li>Understanding the results.</li>
</p></ul>
<hr style="width:50%;text-align:left;margin-left:0">

<h2>CREATING THE DATASET</h2>
<p>The dataset for this project has been generated from 2 major datasets:<br> 
  1. The <a href= "https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia">Kaggle Datset</a> for Normal/Non-Covid X-Rays.<br> 
  2. The <a href= "https://github.com/ieee8023/covid-chestxray-dataset">Datset</a> for COVID X-Rays.
  
Clone the repository given in the second link. From the image folder we extract random X-Rays of <b>PA(posteroanterior)</b> view and store it in our <b>Dataset/Train Data/Covid/</b>.<br>

Download the Kaggle Dataset and from the Normal image folder extract same no:of normal images and store it in out <b>Dataset/Train Data/Non-Covid/</b>.<br>

The Train Dataset has total of <b>284 images</b> where there are <b>142 images</b> each of Covid and Non-Covid.

Do the same for creating <b>Dataset/Test Data/Covid</b> and <b>Dataset/Test Data/Non-Covid</b> but with comparatively lesser no:of images in both. In this project we have considered <b>60 Non-Covid images</b> and <b>55 Covid-Images</b>. Hence a total of <b>115 images</b> in the Test Datset. 


Get the newly created dataset <a href ="https://bit.ly/3f2NUly">here.</a><br>
Or exectute the <b>Dataset Creator.ipynb</b> file to create dataset of your own.</p> 
<hr style="width:50%;text-align:left;margin-left:0">

<h2>DEPENDENCIES</h2>
<p><ul>
  <li>Numpy</li>
  <li>Matplotlib</li>
  <li>Keras</li>
  <li>OS</li>
  <li>Sklearn</li>
  <li>OpenCV</li>
  <li>Seaborn</li>
  <li>Lime</li>
  <li>Time</li>
  <li>Pandas</li>
  <li>Datetime</li>
</ul></p>
<hr style="width:50%;text-align:left;margin-left:0">

<h2>BUILDING THE MODEL</h2>
<p>The CNN Model has been hand coded from scratch. This is a 4-layer CNN. The summary of the model is shown below:<br>
  <img src="https://user-images.githubusercontent.com/35571958/80689714-5a96c780-8aeb-11ea-84e2-2b5626fd2b05.png" alt="model summary"></img></p>
  <hr style="width:50%;text-align:left;margin-left:0">
  
 <h2>UNDERSTANDING THE RESULTS</h2>
 <p>The confusion matrix of the model is given as:<br>
  <img src="https://user-images.githubusercontent.com/35571958/80721061-669a7d80-8b1b-11ea-9556-e0f9ee831ca8.png" alt="Confusion Matrix"></img><br>
  There is scope for improvement of the model accuracy on the validation set.<br>
  The class activation maps the images are given as:<br>
  <img src="https://user-images.githubusercontent.com/35571958/80721559-fdffd080-8b1b-11ea-929c-1701a9ca6869.png" alt="Heat Maps"></img>
  </p><br>
  <p>We use LIME, to explain the predictions of our classifier. <b>LIME</b> is an algorithm that explains the output of any classifier or regressor in a faithful way, by approximating it locally with an interpretable model. It highlights the super-pixels with positive weight towards a specific class, as it gives the intuition as to why the model would think that class may be present.<br>
  The results of the LIME algorithm is given below:<br>
  <img src="https://user-images.githubusercontent.com/35571958/80725138-4caf6980-8b20-11ea-88a8-3163bf91c997.png" alt="Lime Output"></img></p>
  <hr style="width:50%;text-align:left;margin-left:0">
 
 <h2>REFERENCES</h2>
<p><ul>
  <li><a href="https://www.medrxiv.org/content/10.1101/2020.02.14.20023028v5">A deep learning algorithm using CT images to screen for Corona Virus Disease (COVID-19).</a></li>
  <li><a href="https://arxiv.org/pdf/1602.04938.pdf">Why Should I Trust You? Explaining the Predictions of any Classifier.</a></li>
 </ul></p>
 <hr style="width:50%;text-align:left;margin-left:0">
 
 <p>&#169;Contributed by: Souvik Ghosh & Sawon Bhattacharya.</p>
 
  
