# CS 398 Deep Learning @ UIUC

## Homework 6 Understanding CNNs and Generative Adversarial Networks

Name: Yawen Duan		UIN: 655877290

### **HW6 Description:**

The assignment consists of training a Generative Adversarial Network on the CIFAR10 dataset as well as a few visualization tasks for better understanding how a CNN works.

- Train a baseline model for CIFAR10 classification (~2 hours training time)
- Train a discriminator/generator pair on CIFAR10 dataset utilizing techniques from [ACGAN](https://courses.engr.illinois.edu/ie534/fa2018/GAN.html#auxiliary-classifer-gan-acgan) and [Wasserstein GANs](https://courses.engr.illinois.edu/ie534/fa2018/GAN.html#wasserstein-gans) (~40-45 hours training time)
- Use techniques to create synthetic images maximizing class output scores or particular features as a visualization technique to understand how a CNN is working (<1 minute)

### Test Accuracy for discriminators

#### Trained without the Generator

Test Accuracy: **89.29%** after 100 epochs.

![Screen Shot 2019-04-10 at 2.52.29 PM](assets/Screen Shot 2019-04-10 at 2.52.29 PM.png)

#### Trained with the Generator

Test Accuracy: **75.62%** after 200 epochs.

![Screen Shot 2019-04-10 at 2.55.17 PM](assets/Screen Shot 2019-04-10 at 2.55.17 PM.png)

### Output

#### Generator

- I trained the discriminator/generator pair for 200 epochs. Below are some samples of generated images.

**Epoch 0**

![000](assets/000.png)

**Epoch 40**

![039](assets/039.png)

**Epoch 80**

![079](assets/079.png)

**Epoch 120**

![119](assets/119.png)

**Epoch 160**

![159](assets/159.png)

**Epoch 200**

![199](assets/199.png)

#### **Perturb Real Images**

- From **Perturb Real Images**. A batch of real images, a batch of the gradients from an alternate class for these images, and the modified images the discriminator incorrectly classifies.

Below are the images and processed images we retrieved. We found that the classification accuracy on real images is **92.97%**, but that on jittered images is **10.94%**.

**Real images**

![real_images](assets/real_images.png)

**Gradients**

![gradient_image](assets/gradient_image.png)

**Jittered images**

![jittered_images](assets/jittered_images.png)



#### Synthetic Images Maximizing Classification Output

- From **Synthetic Images Maximizing Classification Output**. Synthetic images maximizing the class output. One for the discriminator trained without the generator and one for the discriminator trained with the generator.

**Synthetic images maximizing class output for discriminator trained without the generator:**

![max_class_DwoG](assets/max_class_DwoG.png)

**Synthetic images maximizing class output for discriminator trained with the generator:**

![max_class_DwG](assets/max_class_DwG.png)



#### Synthetic Features Maximizing Features at Various Layers

- From **Synthetic Features Maximizing Features at Various Layers**. Synthetic images maximizing a particular layer of features. Below are the layer 2,4,6,8 features for discriminator trained with and without the generator.

**Layer 2 features for discriminator trained without the generator**:

![max_features_model1_layer2](assets/max_features_model1_layer2.png)

**Layer 4 features for discriminator trained without the generator**:

![max_features_model1_layer4](assets/max_features_model1_layer4.png)

**Layer 6 features for discriminator trained without the generator**:

![max_features_model1_layer6](assets/max_features_model1_layer6.png)

**Layer 8 features for discriminator trained without the generator**:

![max_features_model1_layer8](assets/max_features_model1_layer8.png)

**Layer 2 features for discriminator trained with the generator:**

![max_features_model2_layer2](assets/max_features_model2_layer2.png)

**Layer 4 features for discriminator trained with the generator**:

![max_features_model2_layer4](assets/max_features_model2_layer4.png)

**Layer 6 features for discriminator trained with the generator:**

![max_features_model2_layer6](assets/max_features_model2_layer6.png)

**Layer 8 features for discriminator trained with the generator**:

![max_features_model2_layer8](assets/max_features_model2_layer8.png)