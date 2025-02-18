# DoggieTech Dog Classifier User Guide

## Introduction

DoggieTech Dog Classifier, an application used for identifying the breed of a
dog given a photo. This classifier is trained on the
[Stanford Dogs Dataset](https://www.kaggle.com/datasets/jessicali9530/stanford-dogs-dataset),
and currently uses only three different breed categories.

This user guide discusses the files used in the application and how to interact
with the model via different methods.

To access the remote application, please visit one of the following links:

- ~~[Binder online instance](https://mybinder.org/v2/gh/GCadel/dog_breed_classification/HEAD?urlpath=%2Fdoc%2Ftree%2Fmain.ipynb)~~
  **Binder instance is currently unavailable as of 02/16/2025.**
  - Follow the steps listed under
    [User Instructions (Remote) - Binder](#user-instructions-remote---binder)
- [Replit online instance](https://replit.com/@gcadelm/dogbreedclassification)
  - Follow the steps listed under
    [User Instructions (Remote) - Replit](#user-instructions-remote---replit)

## Overview

The DoggieTech Dog Classifier uses Python and Jupyter Notebooks to download and
parse data, develop and create machine learning models, and provide an interface
for user interaction. Here is how the sections of the application are separated:

- [main.ipynb](./main.ipynb) is the user interface, where a user may upload a
  photo of a dog and retreive the machine learning model's prediction on the
  type of breed the dog is identified as.
- [dataImporting.ipynb](./dataImporting.ipynb) contains the code for downloading
  the
  [Stanford Dogs Dataset](https://www.kaggle.com/datasets/jessicali9530/stanford-dogs-dataset)
  and parsing the data for use in the machine learning algorithm. Generates the
  parsed data as [inputs_and_labels.pickle](./inputs_and_labels.pickle).
  - Under the section **Image formatting helper methods** will be the variable
    `reducedListLabels` which can be modified for more or less dog breeds and
    breed types.
  - After downloading and unzipping the dataset using cell 1-3, you can identify
    available breed annotations in directory
    `sd_dataset\annotations\Annotation`; an example annotation from a directory
    may look like "n02097658-silky_terrier". Use the "silky_terrier" portion of
    the directory name
- [training.ipynb](./training.ipynb) is where the machine learning model is
  built and trained on the dataset. The final trained model is saved for use in
  [trained_models.p](./trained_models.p). This file also generates visual
  statistics about the model such as confusion matrices, image distribution,
  etc.

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
and [Visual Studio Code](https://code.visualstudio.com/) as the interactive for
running the notebook.

### Step 2

Run all the cells in the notebook.
<img src="./md_images/local_01.png" alt='Step 2'>

### Step 3

Scroll to the bottom of **Section 2 in the notebook**. Click the `Upload Photo`
button. <img src="./md_images/local_02.png" alt='Step 3'>

### Step 4

Choose a photo of a dog to be analyzed.

<img src="./md_images/local_03.png" alt='Step 4'>

### Step 5

Click the `Analyze Dog` button. The application will display the output in a new
cell below the `Upload Photo` and `Analyze Dog` buttons.
<img src="./md_images/local_04.png" alt='Step 3'>

<!-- Begin Replit -->

## User Instructions (Remote - Replit)

### Application access

To access the application, please visit the Replit app instance here:

> https://replit.com/@gcadelm/dogbreedclassification

### Step 1

Navigate to the Replit application, then click **Remix this app**.

<img src="./md_images/replit_01.png" alt='Step 1'>

### Step 2

Log into Replit with one of the available options. If necessary, create an
account and perform verification steps Replit asks of you. You may need to
refresh the page to ensure you are logged into Replit, then click **Remix this
app** again.

<img src="./md_images/replit_02.png" alt='Step 2'>

### Step 3

A prompt titled _Remix App_ should appear. Click the blue **Remix App** button
near the bottom.

<img src="./md_images/replit_03.png" alt='Step 3'>

### Step 4

Click the green **Run** button.

<img src="./md_images/replit_04.png" alt='Step 4'>

### Step 5

After a period of waiting, a Webview window should appear. Once visible, click
on the **+** icon next to the Webview tab.

<img src="./md_images/replit_05.png" alt='Step 5'>

### Step 6

Scroll down to find the **Networking** selection, then click on it.

<img src="./md_images/replit_06.png" alt='Step 6'>

### Step 7

A Networking tab should appear above, next to the Webview tab. Click on the
Networking tab, then click on the green link provided.

<img src="./md_images/replit_07.png" alt='Step 7'>

### Step 8

A new browser tab should open to Jupyter Notebook. Find the file `main.ipynb`
and double-click it.

<img src="./md_images/replit_08.png" alt='Step 8'>

### Step 9

Click the link `JupyterLab` on the top-right of the toolbar.

<img src="./md_images/replit_09.png" alt='Step 9'>

### Step 10

Locate the directory icon on the left side of the web application, then click
the icon to open the file tree.

<img src="./md_images/replit_10.png" alt='Step 10'>

### Step 11

Double-click the folder `toClassify` to open the directory in the file tree.

<img src="./md_images/replit_11.png" alt='Step 11'>

### Step 12

Choose a photo of a dog from your computer. You can drag-and-drop the photo from
the computer file explorer into the JupyterLab file tree.

<img src="./md_images/replit_12.png" alt='Step 12'>

### Step 13

Verify the photo has been uploaded.

<img src="./md_images/replit_13.png" alt='Step 13'>

### Step 14

On the toolbar, click (1)`Run` > (2)`Run All Cells`.

<img src="./md_images/replit_14.png" alt='Step 14'>

### Step 15

The browser should automatically scroll down to the bottom of the Python
Notebook. If it has not, scroll down below the last code cell, right before the
cell that says "Section 3: Statistics".

If the page does not match the image below, please wait a moment, as the
application is likely loading. An interface should appear with two buttons and a
drop-down selector.

Click on the drop-down selector.

<img src="./md_images/replit_15.png" alt='Step 15'>

### Step 16

Select the file that matches the image you've uploaded in [Step 12](#step-12)

<img src="./md_images/replit_16.png" alt='Step 16'>

### Step 17

Click the (1)`Analyze Dog` button, then click the blue (2)`log entries` icon.

<img src="./md_images/replit_17.png" alt='Step 17'>

### Step 18

Expand the toolbar for better visibility by clicking and dragging on the thin
grey bar, as shown in the image below.

<img src="./md_images/replit_18.png" alt='Step 18'>

### Step 19

View the result provided by the algorithm.

<img src="./md_images/replit_19.png" alt='Step 19'>
<!-- End Replit -->

## User Instructions (Remote - Binder)

### Application access

To access the application, please visit the Binder online instance here:

> https://mybinder.org/v2/gh/GCadel/dog_breed_classification/HEAD?urlpath=%2Fdoc%2Ftree%2Fmain.ipynb

### Step 1

Locate the directory icon on the left side of the web application, then click
the icon to open the file tree.

<img src="./md_images/run_remote_01.png" alt='Step 2'>

### Step 2

Double-click the folder `toClassify` to open the directory in the file tree.

<img src="./md_images/run_remote_02.png" alt='Step 2'>

### Step 3

Drag and drop the photo of the dog to identify into the folder.

<img src="./md_images/run_remote_03.png" alt='Step 3'>

### Step 4

Verify your photo was uploaded.

<img src="./md_images/run_remote_04.png" alt='Step 4'>

### Step 5

On the top menu bar, click `Kernel` > `Restart Kernel and Run All Cells...`

**NOTE**: You may need to click on / highlight one of the notebook cells first
if the option is not clickable.

<img src="./md_images/run_remote_05.png" alt='Step 5'>

### Step 6

Click `Restart` if prompted.

<img src="./md_images/run_remote_06.png" alt='Step 6'>

### Step 7

Scroll to the bottom of the page. After the last cell, a selection dropdown will
be present. Click on the dropdown and select the photo you've uploaded.

<img src="./md_images/run_remote_07.png" alt='Step 7'>

### Step 8

First, click on the `Analyze Dog` button, then click the blue **log entries**
icon at the bottom of the page.

<img src="./md_images/run_remote_08.png" alt='Step 8'>

### Step 9

Expand the window by clicking and dragging the **thin bar** between the **log
tab** and the **cell view**. Once expanded, you can see the photo you've
uploaded and the predicted label for the given photo underneath.

<img src="./md_images/run_remote_09.png" alt='Step 9'>
