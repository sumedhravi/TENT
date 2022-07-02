# TENT
Training robust Machine Learning models using Test Time Entropy Minimization technique, proposed by [Dequan Wang et al](https://arxiv.org/abs/2006.10726). 

Modern Deep Neural Networks can achieve high accuracy on classification and segmentation tasks when training and testing data is from the same distribution. However, generalization to new and different data is limited and accuracy drops when the testing data differs from the trainingdata distribution, which can be caused by adversarial attacks. This means the model can be deceived quite easily, which could lead to undesirable effects.

This repository consists of code to train a Convolutional Neural Network model on an image dataset and evaluate its performance on clean and noisy data. MNIST dataset was used to train the model and the MNIST-C dataset was used as the noisy data for testing. MNIST-C contains 15 different corruptions of the original MNIST dataset and can be downloaded [here](https://zenodo.org/record/3239543#.YrkHYOzMJEY). 

We observed an improvement in performance for all the model architectures when using TEST during evaluation phase. Trained models have also been included in this repository.

## Comaprison of performance

### Resnet 18 model
![Resnet model comparison with and without applying TENT](/plots/mnistc_resnet18.jpg)
### VGG16 model
![VGG16 model comparison with and without applying TENT](/plots/mnistc_vgg16.jpg)
### Simple CNN model
![Simple CNN model comparison with and without applying TENT](/plots/mnistc_simpleCNN.jpg)

