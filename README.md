# mllab_uni_bonn
Hi!

I took a practical course in machine learning when I was doing my master in mathematics at the University of Bonn and thought it would be a good idea to make a compilation of the different projects and techniques we saw.

Now, I know the folder's names may be a bit criptic and maybe you don't want to go over each one of them to check out if there's something of your interest,so here you have a short summary of what you can find in each one of the folders.

## mmlab-excercise 1

This was an introduction to NumPy sheet: playing around with arrays, generating random numbers with different distributions, working with slices and a bit of linear algebra. Nothing special, but just something to get familiar with one of the main tools we would be using.


## mmlab-excercise 2

In this sheet we started with the proper machine learning material and we kicked off with an oldie but goldie: support vector machines.
We used synthetic data with different probability distributions to try out different algorithms and compare how each of them worked. For instance, here you can see a comparison we made using SMO, LLS and KKT algorithms so classify data from two different exponential distributions


<p align="center">
  <img width="600" height="400" src="https://github.com/JoelVO/mllab_uni_bonn/blob/master/pictures/svm.png">
  <p align="center"> Support vector machines </p>
</p>



Afterwards we analyzed the need of using kernels to be able to handle data described by other distributions. Below you can see how we used a Gaussian kernel to classify data with circular concentric symmetry, highlighting its support and margin definig vectors.


<p align="center">
  <img width="500" height="500" src="https://github.com/JoelVO/mllab_uni_bonn/blob/master/pictures/gaussian_kernel.png">
  <p align="center"> Classification done with a Gaussian kernel </p>
</p>

## mmlab-excercise 3

Moving on, we entered the lowering dimension algorithms and as it's most natural, we started with PCA. Here we experimented with a very nice toy example and the importance on the surface we're projecting on, applied it to the iris data set, saw how the obtained eigenvectors can encode actual information by themselves as in the pedestrian data base, studied how it can be used at the same time as the already familiar support vector machines and finnaly, dived a bit into HOG features.

<p align="center">
  <img width="600" height="200" src="https://github.com/JoelVO/mllab_uni_bonn/blob/master/pictures/eigenpedestrians.png">
  <p align="center"> First ten "eigenpedestrian" obtained with PCA </p>
</p>


## mmlab-excecise 4

It was only a matter of time until we reached neural networks and the time had come.

To get an actually familiar with the topic, we first implemented our own very basic neural network as a class with a backpropagtion and sequential gradient descent functions and played a little bit with it by classifying data with concentric circular symmetry and how, for a given number of iterations, the accuracy would change as we vary our learning rate.

<p align="center">
  <img width="600" height="400" src="https://github.com/JoelVO/mllab_uni_bonn/blob/master/pictures/lr.png">
  <p align="center"> Classification obatined with a fixed number of iterations 
  <br>and changing the learning rate </p>
</p>

But in order to get more serious and having already had our fun, we switched to use keras library and experimented changing learning rates and other parameters to improve our model's accuracy.

Lastly, we revisited our pedestrian data set to compare if it would be better distinguishing is there any on some input picture and then we got challenged to improve the classification by either modyfing the architecture or whatever we could think off. Since I realized the model was over-relaying on finding legs and heads and it was not always the case that you could find that in your pictures (e.g. a car was occluding the legs or a light post the head), I made data augmentation by drawing vertical and horizontal monocromatic lines in my pictures so I could recreate more often the occlusion and thus make my model look for different features.

<p align="center">
  <img width="600" height="400" src="https://github.com/JoelVO/mllab_uni_bonn/blob/master/pictures/augmentation.png">
  <p align="center"> Examples of data augmnetation to boost accuracy </p>
</p>

## mmlab-excercise 5


To finish the lectures, we took a look at reinforcement learning applied to games on the gym library.
In order to do so, we checked how reinforcement learning may interact with neural networks and I taught (not very succesfully if I'm being honest, largely in part because of computational limitations though) a neural network how to play Space Invaders.


<p align="center">
  <img width="300" height="400" src="https://github.com/JoelVO/mllab_uni_bonn/blob/master/pictures/space_invaders.png">
  <p align="center"> Neural network playing Space Inviders</p>
</p>

## Final project

As part of the final grade, we got a needed to do a final project so I did a translator from US sign language to english. To do so, I used YOLOv5 which I fine-tuned to recognize and classify the hands' postures using HaGRID data set [1]. I found a bias in this dataset which made the validation a bit tricky, but eventually I managed to get it working including the cases in which different types of noise are added to the video. 

<p align="center">
  <img width="300" height="400" src="https://github.com/JoelVO/mllab_uni_bonn/blob/master/pictures/final_project_result.mp4">
  <p align="center"> Result for sign language translator</p>
</p>

You can find the whole test video in the "Pictures" folder.

## References

[1] https://www.kaggle.com/datasets/kapitanov/hagrid/code

[2] https://github.com/ultralytics/yolov5

## Recomended literature

O'Neil, C. (2018) Weapons of math destruction how big data increases inequality and threatens democracy. London: Penguin Books. 
