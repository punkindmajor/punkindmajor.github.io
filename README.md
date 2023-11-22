# ECEN 758 Group 31 Project
## Abstract
The goal of this project is to explore the [FashionMNIST](https://github.com/zalandoresearch/fashion-mnist) dataset, and build a data mining pipeline starting from data cleansing to classification. 
We first applied dimensionality reduction technique to better visualize the distribution of data, and also find potential pattern that can help deciding our choice of model and learning method.
We picked [squeezenet](https://pytorch.org/hub/pytorch_vision_squeezenet/) as our model. By leveraging cross validation and multiple experiments we have obtained the best hyperparameters to train our model and the resulting prediction can reach 93% accuracy on the testing set.
## Dataset
As its name suggested, the FashionMNIST dataset is highly inspired by the original [MNIST](https://www.tensorflow.org/datasets/catalog/mnist) dataset, which consists of images of hand-written numbers ranging from 0 to 9.
Like the MNIST dataset, ten classes of grayscale images are included. Unlike the MNIST dataset, the ten classes represent ten different apparels where much more complicated detailed must be learned in order to achieve great accuracy when classifying.
### Why FashionMNIST?
There are two main reasons why researching FashionMNIST might be more favorable comparing to keep using MNIST:
* The MNIST dataset is too easy for most of mordern large models, for example, CNN can reach 99.7% on MNIST with reasonable optimization
* The MNIST is not siutable for some state-of-the-art CV technique, some method might work well on MNIST but does not transfer to real CV data.
### A quick overview on FashionMNIST ###
As mentioned above, FashionMNIST consists of ten classes of apperals, labeled 0~9 corresponding to:
**T-shirt/top, Trouser, Pullover, Dress, Coat,Sandal, Shirt, Sneaker, Bag, Ankle boot.**

And the dataset is separated into two sets, training set and testing set, consists of 60000 and 10000 images respectively.The distribution of Classes on either sets are perfectly balanced,
Here are some example image from FashionMNIST
![example](/Example_images.png)

### Dimensionality Reduction ###
