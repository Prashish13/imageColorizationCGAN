# Colorizing Grayscale Photos using Conditional Generative Adversarial Networks(cGAN) model


<h3><b>Required Libraries</b></h3>
- OpenCV <br>
- OS <br>
- Pickle<br>
- PIL<br>
- Scikit-Image<br>
- Numpy<br>
- Keras<br>
- Matplotlib<br>

<h3><b>Datasets</b></h3>
The images used in this project were downloaded from unsplash.com. Around 1100 coastal images were downloaded and divided into train and test folder later.
The downloaded images were of different size . So, all images were resized into 256 * 256 dimension. PIL is a famous python imaging library, and it was used for resizing images.
After resizing the images, the corresponding grayscale version of all colored(original) images were created using PIL. 
Later, all grayscale and color images were arranged into 2 seperate folder(Gray & Color) and splitted between Train and Val folders.
THe dataset can be found inside <b>Dataset.zip</b>

<h3><b>Model</b></h3>
<b>Conditional generative adversarial network (cGAN) </b>is an extension of the <b>generative adversarial network (GAN)</b> that's used as a machine learning framework for training generative models. The idea was first published in a 2014 paper titled Conditional Generative Adversarial Nets by Mehdi Mirza and Simon Osindero.

CGAN is a deep learning method where a conditional setting is applied, meaning that both the generator and discriminator are conditioned on some sort of auxiliary information such as class labels or data from other modalities. As a result, the ideal model can learn multi-modal mapping from inputs to outputs by feeding it with different contextual information

In this project, I have used Pix2Pix GAN.The Pix2Pix model is a type of conditional GAN, or cGAN, where the generation of the output image is conditional on an input, in this case, a source image. The discriminator is provided both with a source image and the target image and must determine whether the target is a plausible transformation of the source image. The generator is then updated with both adversial loss and L1 loss. Adversial loss helps generator to generate more realistic images in target domain. L1 loss which is measured between generated image and expected output image encourages generator to create more realistic translation of source images.

The architecture and hyperparameter used in this project is described by Philip Isola and his team in the paper entitled <b>"Image-to-Image Translation with Conditional Adversarial Networks".</b> Link:https://arxiv.org/abs/1611.07004

<h4><b>Generator </b></h4>
The generator model is based on the U-net architecture which consist of <b>encoder block layer,bottleneck layer and decoder block</b>.Here, skip connection connects encoding layer and decoding layer.Generator takes input grayscale image and tries to generate corresponding color image.
<b>Image of U-Net Architecture</b>


























![Alt text](plot_030000.png?raw=true "Optional Title")
![Alt text](U-Net.png?raw=true "Optional Title")
