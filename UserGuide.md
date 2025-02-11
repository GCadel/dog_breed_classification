# DoggieTech Dog Classifier User Guide

Thank you for using the DoggieTech Dog Classifier application. This application
can identify the breed of a dog using a provided photo.

Important areas to look at on the webpage are highlighted in red in this guide
for quick identification.

If the application is not running on the local machine and is instead running
remotely (i.e., Binder), please follow the provided steps in the
[Remote User Instruction](#user-instructions-remote) section.

If the application is running locally, please follow the provided steps in the
[Local User Instruction](#user-instructions-local) section.

## User Instructions (Local)

### Step 1

Load the application in your Python Notebook editor of choice. For this example,
the application will be running on a Windows 11 machine with
[Anaconda](https://www.anaconda.com/download) managing the Python environment
and [Visual Studio Code](https://code.visualstudio.com/) as the interactive
interface for running the notebook.

### Step 2

Run all the cells in the notebook. <img src="./local_01.png" alt='Step 2'>

### Step 3

Click the `Upload Photo` button <img src="./local_02.png" alt='Step 3'>

### Step 4

Choose a photo of a dog to be analyzed. <img src="./local_03.png" alt='Step 4'>

### Step 5

Click the `Analyze Dog` button. The application will display the output in a new
cell below the `Upload Photo` and `Analyze Dog` buttons.
<img src="./local_04.png" alt='Step 3'>

## User Instructions (Remote)

### Application access

To access the application, please visit the Binder online instance here:

> https://mybinder.org/v2/gh/GCadel/dog_breed_classification/HEAD?urlpath=%2Fdoc%2Ftree%2Fmain.ipynb

### Step 1

Locate the directory icon on the left side of the web application, then click
the icon to open the file tree.

<img src="./run_remote_01.png" alt='Step 2'>

### Step 2

Double-click the folder `toClassify` to open the directory in the file tree.

<img src="./run_remote_02.png" alt='Step 2'>

### Step 3

Drag and drop the photo of the dog to identify into the folder.

<img src="./run_remote_03.png" alt='Step 3'>

### Step 4

Verify your photo was uploaded.

<img src="./run_remote_04.png" alt='Step 4'>

### Step 5

On the top menu bar, click `Kernel` > `Restart Kernel and Run All Cells...`

<img src="./run_remote_05.png" alt='Step 5'>

### Step 6

Click `Restart` if prompted.

<img src="./run_remote_06.png" alt='Step 6'>

### Step 7

Scroll to the bottom of the page. After the last cell, a selection dropdown will
be present. Click on the dropdown and select the photo you've uploaded.

<img src="./run_remote_07.png" alt='Step 7'>

### Step 8

First, click on the `Analyze Dog` button, then click the blue **log entries**
icon at the bottom of the page.

<img src="./run_remote_08.png" alt='Step 8'>

### Step 9

Expand the window by clicking and dragging the **thin bar** between the **log
tab** and the **cell view**. Once expanded, you can see the photo you've
uploaded and the predicted label for the given photo.

<img src="./run_remote_09.png" alt='Step 9'>
