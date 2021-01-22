# CINIC10 Image Classifier Using CNNs

Goal of this project is to learn how CNNs work and how hyperparameters effect them. In this project, CINIC-10 (an augmented extension of CIFAR-10) dataset from Kaggle will be used. 10 different CNN models will be trained to see success rate differences.


## How The Code Will Be Run

Code file itself is saved as a notebook file. Code requires high processing power. Running this code, in many computers, will take a long time. Recommended way to run this code is to use Google Colab and switch to a GPU runtime enviroment. User may run this code in their own PCs by modifying parts of code that does Google Colab and downloading libraries that aren't downloaded in code itself such as Tensorflow, Numpy and Sklearn. 
Another requirement is to have a Kaggle account, since by using this code you will be downloading the dataset to Google Colab server automatically. At the runtime you will be asked to upload a Kaggle API Token file. You must use a valid token for the code to work properly.

## Models That Will Be Used and Results

10 different model will be tested in total. 6 of them will be trained from scratch. Other 4 will be trained upon VGG and ResNet with minor differences. In all models optimizers will be adam, loss function will be categorical crossentropy, kernel initializers will be GalorotNormal, activation functions will be softmax for output layers and relu for others.
Full list of models with corresponding success rates is:

 - 2 layers of 2D CNN with 3x3 kernel size and 0.2 drop rate. (loss: 0.2955 - accuracy: 0.8977 - val_loss: 2.7475 - val_accuracy: 0.4488)
 - 2 layers of 2D CNN with 3x3 kernel size and 0.7 drop rate. (loss: 1.2038 - accuracy: 0.5709 - val_loss: 1.5213 - val_accuracy: 0.4547)
 - 2 layers of 2D CNN with 5x5 kernel size and 0.2 drop rate. (loss: 0.3396 - accuracy: 0.8818 - val_loss: 2.8176 - val_accuracy: 0.4450)
 - 3 layers of 2D CNN with 3x3 kernel size and 0.2 drop rate. (oss: 0.2089 - accuracy: 0.9267 - val_loss: 2.9499 - val_accuracy: 0.4810)
 - 3 layers of 2D CNN with 3x3 kernel size and 0.7 drop rate. (loss: 1.3388 - accuracy: 0.5191 - val_loss: 1.6569 - val_accuracy: 0.4312)
 - 3 layers of 2D CNN with 5x5 kernel size and 0.2 drop rate. (loss: 2.3027 - accuracy: 0.1011 - val_loss: 2.3026 - val_accuracy: 0.1000)
 - Pretrained VGG model but last layer is trainable (loss: 1.4405 - accuracy: 0.4768 - val_loss: 1.4176 - val_accuracy: 0.4841)
 - Pretrained VGG model but last 4 layers are trainable (loss: 0.7227 - accuracy: 0.7392 - val_loss: 1.1570 - val_accuracy: 0.6182)
 - Pretrained ResNet model but last layer is trainable (loss: 1.7913 - accuracy: 0.3276 - val_loss: 1.8225 - val_accuracy: 0.3217)
 - Pretrained ResNet model but last 4 layers are trainable (loss: 1.8002 - accuracy: 0.3263 - val_loss: 1.8215 - val_accuracy: 0.3205)

For further analysis it is recommended to run the code for yourself. Code provides a confusion matrix and different success rate calculators for different classes (precision, recall and f1 score).

