# DoggieTech Dog Image Classifier

An application used to identify a dog breed.

Open the application here:

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/GCadel/dog_breed_classification/HEAD?urlpath=%2Fdoc%2Ftree%2Fmain.ipynb)

## How to use this application

This is the interactive application where you submit an image of a dog for breed
identification. Please skip to [Section 1](#section-1-pre-use-setup) for
instructions to follow before using the application.

If you already know how to use the application, please skip to
[Section 2](#section-2-using-the-application).

## Section 0: Application Setup

No need to worry about this section. This is where the application setup occurs.
After performing "Run All", jump to [Section 1](#section-1-pre-use-setup) to
start interacting with the application.

## Section 1: Pre-use Setup

This is where you will walk through the the process of using this application.
The steps are as follows:

- Take a picture of the dog.
- Crop the photo _(optional, but may help with accuracy)_.
- Upload the photo to the folder `toClassify`.
- Click the **Analyze Dog** button.

### Part A: Take a photo

Take a picture of the dog you'd like to analyze. The clearer the photo of the
dog, the likelihood of the algorithm correctly identifying the dog breed
increases.

Here's an example of a good photo:

<figure>
<img src="./good_example.jpg" width="300" alt="Good photo of dog">
<figcaption>A clear photo of the dog showing distinct features.</figcaption>
</figure>
<br>
<!-- ![Good Photo of Dog](good_example.jpg "Something") -->

Here's an example of a bad photo:

<figure>
<img src="./bad_example.jpg" alt="Bad photo of dog" width="300">
<figcaption>The dog is obstructed by objects in the photo.</figcaption>
</figure>
<br>
<!-- ![Bad Photo of Dog](bad_example.jpg) -->

**Have a picture ready? Move onto [Part B](#part-b-crop-a-photo-optional)**

### Part B: Crop a photo (optional)

While cropping the photo is optional, it will help increase the accuracy of the
photo analysis. ([Skip this step](#section-2-using-the-application))

Here's an example of an uncropped photo:

<figure>
<img src="./uncropped_example.jpeg" width="300" alt="An uncropped photo">
<figcaption>An uncropped photo of a dog and excessive background space.</figcaption>
</figure>
<br>

Here's an example of a cropped photo:

<figure>
<img src="./cropped_example.jpeg" alt="A cropped photo" width="300">
<figcaption>A cropped photo focused on the dog, reduced background space.</figcaption>
</figure>
<br>

**Have the cropped photo ready?
([Continue to Section 2](#section-2-using-the-application))**

## Section 2: Using the Application

### Upload a photo

Click on the button labeled **Upload** and select the photo you plan to use.
Currently, this application only accepts '.jpg', '.jpeg', and '.png'.

### Analyze the photo

Finally, we'll analyze the photo of the dog to identify its breed. Click on the
**Analyze Dog** button. You'll see the image you've selected and the predicted
breed the program has produced.

**NOTE**: Currently, the algorithm only supports 3 unique breeds:

- Rottweilers
- Golden Retrievers
- Chihuahuas

You can also try out the examples provided in the _toClassify_ folder.

## Section 3: Troubleshooting

If you're having problems trying to upload an image using the remote notebook
application, take a look at the [User Guide](./UserGuide.md)
