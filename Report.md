# Hellooooooooooo

Welcome to the documentation of the ML project.
Here I'll explain all the steps I followed to create this project!!!

## Lets Begin!

### Data Prosecing 

Firstly, I downloaded all the images from the five repositories. I had gathered over 44k images.
However, I deleted 20k images due to issues like wrong pokemon labelling , multiple pokemon, too much background noise, bad quality, fanarts, etc.

Note:The final dataset is not included in this repository

At first i tried to classify all 151 pokemon or by their evolution lines but the results weren't great.
So I simplified the task to classify Pokemon based on their elemental types.

I believe a lot of you know that some Pokemon have dual type. I manually chose a primary type based on my opinion.
So there isn't any Flying class as all flying pokemon have dual type. Moreover there isn't an Ice class or a Ghost class as I had too few images on these classes. 

On the Data Process Notebook you can see some plots of how the images are distributed to each class!!!

## Notebooks

### LDA Notebook

On the LDA Notebook there is the LDA feature extraction with the classic models. At the end there are all the confusion matrices of the results and the hyperparameters used.

The steps were to reduce the images to 64x64 pixels, reduce the features to 100 with PCA and then use LDA to get the final result. At the end all the classical models were applied.
Don't worry that the results aren't great, as LDA can't extract so complicated features from the Pokemon images.
If you want better results increase the number of pixels or try to do LDA directly.

### Autoencoder Notebook

On the Autoencoder Notebook I trained an autoecnoder for up to 100 epochs, but early stopping kicked in around 30 epochs.
Then I did the same as to the LDA Notebook. Of course I got better results!!!

### MLP_CNN Notebook

In this Notebook things get more interesting. I moved on to training deep learning models. Each one was set to train for up to 100 epochs, but early stopping usually kicked in around epoch 30.
The MLP was trained on the features from the Autoencoder I mentioned earlier. 

The CNN model got even better results than the MLP, thanks to its sliding filter windows, the CNN could detect important patterns across the image.

But the best model was the Deep CNN, as it extracts all the features from it's own. This model was by far the best, reaching an accuracy of 89%! 

That's all Folks!

Have a nice read and try to experiment as you wish!!!
