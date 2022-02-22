# Ganimons
This is a diary of sorts for a small learning project that i'm dabbling in for fun.
The objective is to generate images using a very small dataset of pokemon sprites (<1k images) using generative adversarial networks (GANs).

The main limitation since the dataset is very limited in size, is that the discriminator (which is just a classifier) quickly overfits on the training data.


The few ideas I explored/I'm exploring are :
- Training a DC-GAN using an encoded representation of the data (using an autoencoder), but i quickly realised that capturing the distribution of the observed data would be challenging using only a reconstruction loss. (Currently learning more about regulized autoencoders CAEs RCAEs [Alain, Guillaume & Bengio, Y.. (2012). What Regularized Auto-Encoders Learn from the Data Generating Distribution. Journal of Machine Learning Research. 15. ] ).

- Using differentiable transformations to augment the data [arXiv:2006.10738v4] gave promising results, as the training is stable, but the model needs further training (currently on 600 epochs).
 

- Projected GANs [Sauer, Axel, et al. "Projected gans converge faster." Advances in Neural Information Processing Systems 34 (2021).]are a classic solution that I learned about recently. (I thought I had a weirdly specific idea to train a generative model on images from a game that I like a lot but apparently I was late to the party xD). The idea behind these networks is using multiple discriminators for the different levels of features, and projecting the real/generated images onto these different feature spaces before running them through the discriminators (hence the name).


Please excuse the lack of order in the colab file as it serves as a test sheet for now.




