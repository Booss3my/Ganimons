# Ganimals
Training a generative model on a very small dataset using an autoencoder


In this small project, i've given myself the challenge to train a DC-GAN using sprites from one of the best Pokemon games: Black 2 (in my opinion :) ).

The main limitation is the size of the available data (~<1000 4x96x96 images).

Data augmentation is possible, but keeping in mind the result we hope to obtain at the output of the generative model, which is high quality sprites, consistant with the style and quality of the original data we eliminate some of the augmentation methods such as scaling, cropping, padding, changing brightness, contrast ... For now we'll keep Data Augmentation aside as it affects the quality of the generation.

The second idea I had is to compress this Data to a very small scale, then use it to train an accordingly small generative model.

We'll proceed by training the autoencoder first then combining the generative model and the autoencoder (the autoencoder parameters will be kept constant for the first cycles, once the generator is able to generate acceptable quality images we'll train the model as whole)
