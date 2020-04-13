Project to implement a GAN in PyTorch. Both the generator and the discriminator consist of linear layers (no CNNs) with dropout. We trained it for 100 epochs on the MNIST dataset. Following is sample of images generated by the GAN at the end of training. 

![generated_images](generated_images/gan_mnist_generated_samples.png)

We can see that the images generated by the GAN, though not spectacular, are still quite discernable. Given that we did not use any convolutional layers, this is still an acceptably good performance by our GAN. 

An interesting thing to notice though is that the GAN failed to train at all when I used BatchNormalizaton instead of Dropout. This is opposed to the case in DCGAN where adding BatchNormalization is highly recommended. On the otherhand, this is similar to my earlier implementation of GANs (with only linear layers) in keras as found [here](https://github.com/praritagarwal/GAN-Fashion-MNIST). There also, the GAN did not seem to do a good job of generating Fashion-MNIST images when using BatchNormalization but worked very well once BatchNormalization was traded for Dropout. 

This project was part of the gan-mnist-exercise in Udacity's "Deep Learning with PyTorch" nanodegree.