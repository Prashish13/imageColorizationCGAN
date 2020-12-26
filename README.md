# Colorizing Grayscale Photos using Conditional Generative Adversarial Networks(cGAN) model


<h4><b>Required Libraries</b></h4>
- OpenCV <br>
- OS <br>
- Pickle<br>
- PIL<br>
- Scikit-Image<br>
- Numpy<br>
- Keras<br>
- Matplotlib<br>

<h4><b>Datasets</b></h4>
The images used in this project were downloaded from unsplash.com. Around 1100 coastal images were downloaded and divided into train and test folder later.
The downloaded images were of different size . So, following code will resize all the images into 256 * 256 dimension. PIL is a famous python imaging library, and it was used for resizing images.
After resizing the images, the corresponding grayscale version of all colored(original) images were created using PIL. 
Later, all grayscale and color images were arranged into 2 seperate folder(Gray & Color) and splitted between Train and Val folders.
































![Alt text](plot_030000.png?raw=true "Optional Title")
