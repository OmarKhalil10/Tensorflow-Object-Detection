# Tensorflow Object Detection Walkthrough
<p>This set of Notebooks provides a complete set of code to be able to train and leverage your own custom object detection model using the Tensorflow Object Detection API.
<br/><br/>
<img src="https://i.imgur.com/iE8PZlo.jpeg">
<br/><br/>

# Automatic Number Plate Recognition using Tensorflow and EasyOCR
## Steps:
### Prepare a folder to clone the repository
<b>-<b> Open Cmd then select the disk to create your project folder.
<pre>
c:\Users\User>G:
</pre>
<b>-<b> Crate your folder using: mkdir ANPR.
<pre>
Ex: G:\>mkdir ANPR
</pre>
<b>-<b> Change your Directory to ANPR using cd ANPR.
<pre>
Ex: G:\>cd ANPR
</pre>
<b>-<b> Start Jupyter Notebook by typing (jupyter notebook).
<pre>
Ex: (anprsys) G:\ANPR>jupyter notebook
</pre>
<br/>
<b>Step 1.</b> Clone this repository: https://github.com/OmarKhalil10/Tensorflow-Object-Detection
<br/><br/>
<b>Step 2.</b> Create a new virtual environment 
<pre>
python -m venv anprsys
</pre> 
<br/>
<b>Step 3.</b> Activate your virtual environment
<pre>
source anpr/bin/activate # Linux
.\anprsys\Scripts\activate # Windows 
</pre>
<br/>
<b>Step 4.</b> Install dependencies and add virtual environment to the Python Kernel
<pre>
python -m pip install --upgrade pip
pip install ipykernel
python -m ipykernel install --user --name=anprsys
</pre>
<br/>
<b>Step 5.</b> Collect images using the Notebook <a href="https://github.com/OmarKhalil10/Tensorflow-Object-Detection/blob/main/1.%20Image%20Collection.ipynb">1. Image Collection.ipynb</a> - ensure you change the kernel to the virtual environment as shown below
<img src="https://i.imgur.com/skBbV8c.png"> 
<br/>
<b>Step 6.</b> Manually divide collected images into two folders train and test. So now all folders and annotations should be split between the following two folders. <br/>
\ANPR\Tensorflow\workspace\images\train<br />
\ANPR\Tensorflow\workspace\images\test
<br/><br/>
<b>Step 7.</b> Begin training process by opening <a href="https://github.com/OmarKhalil10/Tensorflow-Object-Detection/blob/main/2.%20Training%20and%20Detection.ipynb">2. Training and Detection.ipynb</a>, this notebook will walk you through installing Tensorflow Object Detection, making detections, saving and exporting your model. 
<br /><br/>
<b>Step 8.</b> During this process the Notebook will install Tensorflow Object Detection. You should ideally receive a notification indicating that the API has installed successfully at Step 8 with the last line stating OK.  
<img src="https://i.imgur.com/yBoGevK.png">
If not, resolve installation errors by referring to the <a href="https://github.com/OmarKhalil10/Tensorflow-Object-Detection/blob/main/Error%20Guide.md">Error Guide.md</a> in the Tensorflow-Object-Detection.
<br /> <br/>
<b>Step 9.</b> Once you get to step 6. Train the model, inside of the notebook, you may choose to train the model from within the notebook. I have noticed however that training inside of a separate terminal on a Windows machine you're able to display live loss metrics. 
<img src="https://i.imgur.com/vzCXsJS.png"> 
<br />
You can see Jupyter Notebook logs for Training on cmd here.
<img src="https://i.imgur.com/AIvPZxf.png"> 
<br />
<b>Step 10.</b> You can optionally evaluate your model inside of Tensorboard. Once the model has been trained and you have run the evaluation command under Step 7. Navigate to the evaluation folder for your trained model e.g. 
<pre> cd Tensorlfow/workspace/models/my_ssd_mobnet/eval</pre> 
and open Tensorboard with the following command
<pre>tensorboard --logdir=. </pre>
Tensorboard will be accessible through your browser and you will be able to see metrics including mAP - mean Average Precision, and Recall.
<br />
