# Binary-Image-Classification
Use of "tensorflow" to apply CNN (Convolutional Neural Network) for binary image classification

This was done as part of Neural Networks Course (BITS Goa), Fall 2019. Scoring was done on Kaggle 
(https://www.kaggle.com/c/nnfl-assignment-i).

# Task: Binary image classification

# Data: 
-> Around 16000 images with their classes (0 or 1)
-> Images were either an indoor or an outdoor image

# Procedure:
-> Data was clean and required no treatment.
-> Converted images to 128x128x3 matrix.
-> Used one hot encoding for classes.

# Model:
_________________________________________________________________
Layer (type)                 Output Shape              Param #   

=================================================================

conv2d_4 (Conv2D)            (None, 126, 126, 32)      896       
_________________________________________________________________
max_pooling2d_4 (MaxPooling2 (None, 63, 63, 32)        0         
_________________________________________________________________
conv2d_5 (Conv2D)            (None, 60, 60, 32)        16416     
_________________________________________________________________
max_pooling2d_5 (MaxPooling2 (None, 30, 30, 32)        0         
_________________________________________________________________
conv2d_6 (Conv2D)            (None, 26, 26, 64)        51264     
_________________________________________________________________
max_pooling2d_6 (MaxPooling2 (None, 13, 13, 64)        0         
_________________________________________________________________
flatten_2 (Flatten)          (None, 10816)             0         
_________________________________________________________________
dense_3 (Dense)              (None, 64)                692288    
_________________________________________________________________
dropout_2 (Dropout)          (None, 64)                0         
_________________________________________________________________
dense_4 (Dense)              (None, 2)                 130

=================================================================
Total params: 760,994
Trainable params: 760,994
Non-trainable params: 0
_________________________________________________________________


-> Epochs = 200
-> Batch Size = 256
-> Activations used were 'relu' and 'sigmoid'(for last dense layer)

#Results : 99.03498 %
