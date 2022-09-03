What is a GAN?
GANs are a framework for teaching a DL model to capture the training data’s distribution so we can generate new data from that same distribution. 
GANs were invented by Ian Goodfellow in 2014 and first described in the paper Generative Adversarial Nets. 
They are made of two distinct models, a generator and a discriminator. The job of the generator is to spawn ‘fake’ images that look like the training images.
The job of the discriminator is to look at an image and output whether or not it is a real training image or a fake image from the generator. 
During training, the generator is constantly trying to outsmart the discriminator by generating better and better fakes,
while the discriminator is working to become a better detective and correctly classify the real and fake images. 
The equilibrium of this game is when the generator is generating perfect fakes that look as if they came directly from the training data, 
and the discriminator is left to always guess at 50% confidence that the generator output is real or fake.

What is a DCGAN?
A DCGAN is a direct extension of the GAN described above, except that it explicitly uses convolutional and convolutional-transpose layers in the discriminator and generator, respectively.
It was first described by Radford et. al. in the paper Unsupervised Representation Learning With Deep Convolutional Generative Adversarial Networks.
The discriminator is made up of strided convolution layers, batch norm layers, and LeakyReLU activations.
The input is a 3x64x64 input image and the output is a scalar probability that the input is from the real data distribution.
The generator is comprised of convolutional-transpose layers, batch norm layers, and ReLU activations.
The input is a latent vector, zz, that is drawn from a standard normal distribution and the output is a 3x64x64 RGB image.
The strided conv-transpose layers allow the latent vector to be transformed into a volume with the same shape as an image.
.
