Firstly, I downloaded the dataset from Kaggle to google drive then unzipped and install it there. After loaded the dataset images from google colab going through the right directory and taking the image and masks ![NNI Screenshot](https://github.com/dvw4/Project/blob/Milestone2/63/1.1.png). Then read each image as BGR in blue,green,red color and dividing it to the patch sizzewhich is 256.  Then used the patchifying library to extract patches from each image. Then did the same exact thing with masks. Then the given color code for buildings.land, road, vegetation, water and unlables was converted into RBG array and then given the labels. Where then just to make sure checked the image if it was as expected  

Where it was good. Then from the other file simple_multi_unet_model we impoerted the multi_unetmodel and jacard coef where the image model was made with height width channels and then was compiled in optimizer ‘adam’ where is all the patches of images were checked and given they are all multiples 256 since our patch size was 256. Then the model was loaded in history1 and then did model fir with batch size of 16 and epochs of 100.![NNI Screenshot](https://github.com/dvw4/Project/blob/Milestone2/63/1.2.png).  Where I received the accuracy of 61.62 percent. 
Then tested for training and validation loss 
 ![NNI Screenshot](https://github.com/dvw4/Project/blob/Milestone2/63/1.3.JPG)
Although not required but also plotted the Graph for IOU
 ![NNI Screenshot](https://github.com/dvw4/Project/blob/Milestone2/63/1.4.png)
 And finally I get this results
 
 ![NNI Screenshot](https://github.com/dvw4/Project/blob/Milestone2/63/1.JPG)
  ![NNI Screenshot](https://github.com/dvw4/Project/blob/Milestone2/63/2.JPG)
 ![NNI Screenshot](https://github.com/dvw4/Project/blob/Milestone2/63/3.JPG)
 ![NNI Screenshot](https://github.com/dvw4/Project/blob/Milestone2/63/4.JPG)
  ![NNI Screenshot](https://github.com/dvw4/Project/blob/Milestone2/63/5.JPG)

