CS 4372 Assignment 3 -- Image Based Project

1) Import Modules and Data
   - In this project, we utilized the following modules:
       - TensorFlow for Deep Learning
       - os, zipefile, requests, BytesIO for data/file loading and handling
       - matplotlib for plotting history/performance curves
       - pandas and numpy to track historical data and visualize testing points
    - The dataset used was a sports balls image classification set from Kaggle.
       - There were 15 different sports balls classes, but we decided to use 3 classes (american_football, baseball, and basketball)
       - There are 1124 training images and 282 testing images in the dataset with the 3 classes chosen
       - **Link:** _https://www.kaggle.com/datasets/samuelcortinhas/sports-balls-multiclass-image-classification?select=train_
    - To run the code, the user can run through the notebook named Project_3_Code. The data is loaded publicly via the github repository
      
3) Model Building/Tuning/Evaluation (Configuration Set 1: **5 models**)
     - Initially, a train_model function is defined with a pre-trained MobileNetV2 model loaded via Keras
         - The train_model function defines possible tuning and builds a model with the base model + extra layers
         - Selects the optimizer based on user input, compiles the model, and implements early stopping to reduce overfitting and enhance computational efficiency
         - The training/testing accuracy and loss are tracked for each model
     - The first set of configurations are focused on tuning the model with changes in dense_units, dropout, learning rate, and layer freezing with a small number of epochs
     - Plots are created using matplotlib to visualize the model's training/testing accuracy and loss across epochs

4) Model Building/Tuning/Evaluation (Configuration Set 2: **2 models**)
     - The train_model function is used again for the second set of configs, but the second set tunes the top 2 performing models from the first set with additional changes to enhance performance
     - The number of epochs are increased to 30 with early stopping to ensure that the model converges efficiently
     - Plots are created using matplotlib to visualize the models
     - The result_final table shows the 7 total configurations used in the notebook with their training/test accuracies and run-times
  
5) Finally, 25 testing points are visualized at random with their image, actual label, and predicted label to understand model performance further
