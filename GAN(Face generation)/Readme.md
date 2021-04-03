# Face Generation using GAN 

- We use two Networks here one is Generator which takes random noize for inspiration and tries to 
generate a face sample , Second is Discriminator which takes a face sample and tries to tell if it's real or fake.
i.e it predicts the probability of input image being a real face.
## Training :
- Train the discriminator to better distinguish real data from current generator.
- Train the generator to make discriminator think generator is real.
- Since , the discrimantor is a differentiable neural network , we train both with gradient descent
- Training is done iteratively until discriminator is no longer able to find the difference(or until we want)
