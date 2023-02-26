Repo consists of 5 notebooks:

1 - CNN_TransferLearning_Muffin_Chihuahua.ipynb - I am using transfer learning from Inceptionv3 (https://keras.io/api/applications/inceptionv3/). The data has been downloaded from Kaggle, and standard means such as ImageDataGenerator with warious augmentation functions has been provided. The training has not been done on top of the last layer but by unfreezing of more layers on top of layer 'mixed7' , even I intended to run 100 epoches, using Callback the accuray 98.5% has been reached after one epoch. 

2 - LSTM_Covid_prediction.ipynb - Long Short-Term NN has been used to predict covid cases. I was not using moving average but only standard time series. The data has been cleaned (only Kosice area has been used) and scalled with MinMax scaler. Small LSTM NN has been build with short training. Mean Average Error is 272.1906 cases, so quite high and the training to be repetated with more Epoches. 

 3 - NLP_text_generator-Sladkovic_Marina_.ipynb - short GAN of NLP has been build to predict Sladkovic's poetry based on his poem Marina - intentionally chosen as this is the longest poem in Slovak language to have better dataset. Data has been cleaned, tokenized and padded. Using LSTM small DNN has been built.

4 - EDA_CNN_Tumor_detection.ipynb - Tumor detection on data from Kaggle. First basic analysis of the dataset with some wrangling and adjustement. Then by means of OOP created a class to use only instances for various classifiers for transfer learning on top layer for ResNet40, Inception V3 and Mobilenet V1. The training performed on Google colab GPU and the best results obtained for Inception V3 on valid data with accuracy 96%. However, once using test data (never seen images from google) the model failed - model overfitted. Some ideas from Kaggle collected about learning rate scheduling, focal loss instead loss function and balancing the dataset - to be used on next notebook.

5 - DNN_GridSeachCV_for_DNN_hyperparamaters.ipynb - I am using the standard dataset from Kaggle "California housing prices" for regression I have already used for other notebook. The data have been normalized as the distribution was quite skewed and some small adjustemnts done along. In this notebook I am using GridSearchCV for DNN Tensorflow model wrapped by KerasRegressor from SciKeras lib (there were similar wrapper from ScikitLearn which is not supported anymore. I have to tune n. of hidden layers, n. of neurons in these layers and learning rate of Adam optimizer. To shorten time there were only 25 Epochs done and as results we got the best parameters of learning rate 0.001, 4 hidden layers with each layer having 64 neurons. 
