For our model, we were tasked with implementing knowledge distillation, where we developed a student learning model from a teacher model, as well as performed model compression.  To begin with we imported all out necessary dependencies from tensorflow and set a number of precautions such as checkpoints, early stopping if needed, and reducing the learning rate when we hit a plateau, all to ensure that our accuracy rate would produce relevant within our model.Upon, obtaining our model summary, we got 865,606 total parameters, all of which we noted were trainable (meaning we had 0 non-trainables values).  Following, we set up our training model, fitting our X and y training data to our teacher model. We then used Kera’s Conv2D method to create our convolution kernel and obtain outputs. We set out a number of filters to learn from to a variety of different depths when setting each layer, however, some constants that we kept throughout all our layers were our padding, activation, and initialization. Max pooling was also added as a means to only obtain our standard presence of each feature. Upon finishing the setup of all of our layers, we developed our model, specifying within it which were our input layers and which were our output convolutions. 
Lastly, we built our teacher and student models, where we established a path to our previous keras tensor values, passing in prior inputs we defined. These values for used for optimizing and retraining, saving our results to our student model. 
