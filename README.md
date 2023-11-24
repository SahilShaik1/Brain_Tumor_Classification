# Brain Tumor Classification

- Convolutional Neural Network Model implemented on a Brain Tumor Classification Dataset, roughly 93% accurate with only 63 batches and 20 epochs used for training

# How to Run
You could directly download the code
- Click on "Raw" after opening the file, and save it as an .ipynb file
- Download the [database](https://github.com/SartajBhuvaji/Brain-Tumor-Classification-DataSet/) off of github
- Link your download location within the code
- Run your file on an application that can run .ipynb files such as Jupyter Notebook
<br>

You could also choose to create a [notebook from Kaggle](https://www.kaggle.com/datasets/sartajbhuvaji/brain-tumor-classification-mri/data)
- Click the "New Notebook" option
- Manually Copy & Paste each code block
- Click "Run All" when you are done

# Architecture
![Typical-CNN-Architecture-1024x374](https://github.com/SahilShaik1/Brain_Tumor_Classification/assets/89698739/c771e8c8-c5b3-4030-a057-64a6b222caa5)

- The tensorflow model uses 3 [convolutional layers](https://www.tensorflow.org/api_docs/python/tf/keras/layers/Conv2D) along with 3 [maximum pooling layers](https://www.tensorflow.org/api_docs/python/tf/keras/layers/MaxPooling2D) in order to detect distinctive features within the image along with using the getting the most prominent feature every time with the [ReLU](https://en.wikipedia.org/wiki/Rectifier_(neural_networks)) activation function
- This is then flattened and directly applied into a fully connected Dense Layer, with 256 units applying the relu activation function in order to convert the tensor recieved from the convolution into something more workable
- This is then finally connected into a 4 unit Dense Layer, applying the [softmax](https://en.wikipedia.org/wiki/Softmax_function) activation function in order to convert all recieving values into probabilites that can be used to predict the class of an image
- The model uses image values between 0-1 and is trained off of 4 images at a time, being considered 1 batch
