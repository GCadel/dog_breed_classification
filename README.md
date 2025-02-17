# DoggieTech Dog Image Classifier

An image classification application used to identify a dog breed.

Replit Access

> https://replit.com/@gcadelm/dogbreedclassification

~~Binder Access~~ **Binder instance is not available as of 02/16/2025**:

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/GCadel/dog_breed_classification/HEAD?urlpath=%2Fdoc%2Ftree%2Fmain.ipynb)

## How to use this application

All instructions for running the application can be found in the
[User Guide](./UserGuide.md)

## Image Setup

This application has some sample images available. Here's what you need to do if
you want to use your own images:

- Take a picture of the dog.
- Crop the photo _(optional, but may help with accuracy)_.

### Taking a photo

Take a picture of the dog you'd like to analyze. The clearer the dog's photo,
the likelihood of the algorithm correctly identifying the dog breed increases.

Here's an example of a good photo:

<figure>
<img src="./good_example.jpg" width="300" alt="Good photo of dog">
<figcaption>A clear photo of the dog showing distinct features.</figcaption>
</figure>
<br><br>
<!-- ![Good Photo of Dog](good_example.jpg "Something") -->

Here's an example of a bad photo:

<figure>
<img src="./bad_example.jpg" alt="Bad photo of dog" width="300">
<figcaption>The dog is obstructed by objects in the photo.</figcaption>
</figure>
<br><br>
<!-- ![Bad Photo of Dog](bad_example.jpg) -->

### Crop the photo (optional)

While cropping the photo is optional, it will help increase the accuracy of the
photo analysis.

Here's an example of an uncropped photo:

<figure>
<img src="./uncropped_example.jpeg" width="300" alt="An uncropped photo">
<figcaption>An uncropped photo of a dog and excessive background space.</figcaption>
</figure>
<br><br>

Here's an example of a cropped photo:

<figure>
<img src="./cropped_example.jpeg" alt="A cropped photo" width="300">
<figcaption>A cropped photo focused on the dog, reduced background space.</figcaption>
</figure>
<br><br>

## Section 2: Using the Application

### Photo Requirements

Currently, the application only accepts the following image formats:

- '.jpg'
- '.jpeg'
- '.png'

Currently, the algorithm only supports 3 unique breeds:

- Rottweilers
- Golden Retrievers
- Chihuahuas

## Section 3: Troubleshooting

If you're having problems uploading an image using the remote Notebook
application, refer to the [User Guide](./UserGuide.md).

## Section 4: Model Statistics

Here are the machine learning model statistics. These are dynamically updated
each time the model is trained to ensure consistency with the model and results
posted.

### Confusion Matrix

Confusion matrices tell us how the model performed during the testing phase.

- The x-axis identifies what dog breed the model predicted given an image.
- The y-axis shows the count of each breed type.

Reading from the top-left square diagonally to the bottom-right square, the
matrix identifies how many of the predictions the model made were correct. The
higher the value, the better the model accuracy.

- Ex: The model correctly predicted a picture of a chihuahua as a chihuahua.

The squares outside of the diagonal identify the amount of times the model
incorrectly predicted a breed type. The lower the value the higher the model
accuracy.

- Ex: Out of **n** images provided of the breed _chihuahua_, the model
  classified the images **k** times incorrectly as the breed _rottweiler_ or
  _golden retriever_.

This is the confusion matrix of the model when trained using a _Random Forest
Classifier_:

<figure>
<img src="./confusion_matrix_results_rfc.png" alt="RFC Confusion Matrix" width=500>
<figcaption>A confusion matrix of the model trained using Random Forest</figcaption>
</figure>
<br><br>

This is the confusion matrix of the model when trained using a _Support Vector
Classifier_:

<figure>
<img src="./confusion_matrix_results_svc.png" alt="SVC Confusion Matrix" width=500>
<figcaption>A confusion matrix of the model trained using Support Vector Classifier</figcaption>
</figure>
<br><br>

### Image Distribution

The image data used to train the model is based on the
[Stanford Dogs Dataset](https://www.kaggle.com/datasets/jessicali9530/stanford-dogs-dataset).
Model training relied on numerous pictures of dogs in the following categories:

- Chihuahua
- Rottweiler
- Golden Retriever

The image distribution of the different dog breeds is similar in size. However,
the amount of sample images available was very low, and the breed within the
images varied greatly (i.e., short-haired chihuahuas and long-haired chihuahuas,
puppies and adults, fur color, etc.).

<figure>
<img src="./dog_breed_distribution.png" alt="Image Distribution Pie Chart" width=500>
<figcaption>A pie chart of the image distribution used by the model during training.</figcaption>
</figure>
<br><br>

### Decision Tree Model

The model had no features to use during the training and testing phase of
development. The model would classify dog breeds based on the pixel density of
images. The model would learn to identify patterns in the pictures that would
lead it to a conclusion for classifying a dog's breed. Decision trees are
created during training and help the model branch to different conclusions when
analyzing the pixel density of the images.

During testing, the random forest classifier (RFC) often outperformed the
support vector classifier (SVC), which led to the decision to use RFC for the
developed model.

This is an example decision tree used in the final version of the machine
learning model:

<figure>
<img src="./rfc_random_decision_tree.png" alt="Decision Tree" width=500>
<figcaption>A decision tree chosen at random for viewing the model's decisions when assessing an image.</figcaption>
</figure>
<br><br>
