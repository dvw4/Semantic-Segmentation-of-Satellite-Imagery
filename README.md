# Project
CS301 Project
By Durgesh Wani, Jason Morales
For our model, we were tasked with using hyperparameter optimization through the method SMAC. Prior to implementing the method though, we preprocessed our data using standard Unet where we built our model and normalized our inputs.These inputs were the image height,width, and channels. We then set a contraction path and an expansive path using the Keras library’s Conv2D parameter, to set the number of kernels that needed to be applied to our images, to later vonvolve each with the input volume and obtain its corresponding activation map. In addition, we used max pooling to aid within the reduction of the spatial dimensions encountered in the output’s volumes. To be able to easily test against various loss functions we decided to compile the model within our main program.
We then set up all of our utilities by importing all dependencies that we would be using within our configuration space and implemented filtering by setting ordinal and uniform hyperparameters. Once these were set, we placed them into our model through a multi Unet model, specifying each filter and passing them in as parameters to it. Factors that we took into consideration when training our model’s fit were our x and y training values, batch_size, verbose, epochs, loss, and validation accuracy. All being set, we capped our maximum function evaluation for epochs at 200, but upon running out of GPU throughout runtime, cut it down to only 50 epochs. Below is our rendered image output, which gave us an accuracy rate of approximately 78 percent. Where we also observed a mean IoU of 0.5015257.
![mean iou](https://github.com/dvw4/Project/blob/Milestone3/mile3/meaniou.jpg)
![addding output](https://github.com/dvw4/Project/blob/Milestone3/mile3/1.jpg)
![addding output](https://github.com/dvw4/Project/blob/Milestone3/mile3/2.jpg)
![addding output](https://github.com/dvw4/Project/blob/Milestone3/mile3/3.jpg)
![addding output](https://github.com/dvw4/Project/blob/Milestone3/mile3/4.jpg)

  
  
  
  
  

Other information we concluded is pictured below, which is our training v. validation graph and our SMAC scores.
Within our training v. validation graph we saw an optimized value of 0.23 and our SMAC Scores graph demonstrates the difference between our model pre-optimization vs. post-optimization (noted within the relationship of our plotted observed scores and number of iterations).

![ioo](https://github.com/dvw4/Project/blob/Milestone3/mile3/mil3.jpg)
![ioro](https://github.com/dvw4/Project/blob/Milestone3/mile3/mile31.jpg)


