INSTALLATION PROCEDURE:
Step 1: Install Pytorch from any browser
![web](https://user-images.githubusercontent.com/91653071/213634923-85471524-0b85-4454-8c10-36a2959e38da.gif)

Step 2:- Install project requirements in the command line.

REQUIREMENTS OF PROJECT:
●	numpy
●	pandas
●	Flask
●	Pillow
●	gunicorn==20.0.4
●	torch==1.8.0
●	torchvision==0.9.0
PROCESS:
The process for building a model which can detect the disease associated with the leaf image. The key points to be followed are:
1.	Data gathering
The dataset taken was "New Plant Diseases Dataset". It can be downloaded through the link "https://www.kaggle.com/vipoooool/new-plant-diseases-dataset". It is an Image dataset containing images of different healthy and unhealthy crop leaves.
2.	Model building
○	I have used pytorch for building the model.
○	I used three models:-
a.	The CNN model architecture consists of CNN Layer, Max Pooling, Flatten a Linear Layers.
b.	Using Transfer learning VGG16 Architecture.
c.	Using Transfer learning resnet34 Architecture.
3.	Training
The model was trained by using variants of above layers mentioned in model building and by varying hyperparameters. The best model was able to achieve 97.5% of test accuracy.
4.	Testing
The model was tested on a total of 17572 images of 38 classes.


 Plants: 'Tomato',  'Apple',  'Blueberry',  'Grape', 'Peach', 'Corn', 'Cherry', 'Squash', 'Strawberry', 'Pepper', 'Orange', 'Potato', 'Raspberry', 'Soybean'

The dataset contains:
* 70295 training images
* 17572 testing images

Workflow:
1. Loading the images from the folder resizing them into 128 * 128 (256 * 256 takes time for processing) and converting them to tensors 
2. Building a validation dataset using 0.3% of the total dataset.
3. Loading the data using Batches
4. Trying various CNN architecture
  * Combination of Multilayer CNN with Linear Layers
  * VGG16 using Transfer Learning
  * Resnet34 using Transfer Learning
5. Selecting the device and loading the data into device i.e (GPU) 
6. Training the model and evaluating the model on test data
