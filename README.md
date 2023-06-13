# AI4Mars Image Segmentation

Starter code used: https://www.kaggle.com/datasets/yash92328/ai4mars-terrainaware-autonomous-driving-on-mars 
Paper Idea: https://data.nasa.gov/api/views/cykx-2qix/files/247093ee-6bcd-45df-8b61-04f13b0346ac?download=true&filename=AI4Mars-AI4Space-final.pdf

This experiment aims to create a Machine Learning model capable of image
segmentation using a convolutional neural network (CNN) to classify images from the
AI4MARS MSL data set. This dataset was built for training and validating terrain
classification models for mars and is useful to train robots for terrain navigation. It contains
35K images with crowdsourced labels. The main goals of this project were to create an
efficient model to compare to the one from the original paper, estimate the impact of the
size of the crowdsourced data set on the training and experiment with models of different
CNN architecture. In my experiment, I used the k-fold cross validation on four CNN
architectures to choose the best architectures by evaluating the average validation
accuracy, loss and validation variance. I tested the validation performance on different
training sizes (representing crowdsourced data size). I also conducted experiments on the
three test datasets using the best CNN model (Model 2) which was the U-Net inspired
CNN architecture. Finally, I trained the remaining three models to evaluate their prediction
performance on the test sets and computed the confusion matrices and segmentation
image examples for all four models to compare. The results showed that the model with
the U-Net inspired CNN architecture (Model 2) could correctly segment and classify
75.07% of the test data and also yielded strong confusion matrices. The test on the impact
of the size of the dataset showed that smaller datasets would affect the model’s learning of
underrepresented labels. Finally, the experiments on multiple models concluded that
model3 and model4 (both of them are U-Net architecture using pre-trained weight) actually
outperform model2 after training for 150 epochs each.


 
