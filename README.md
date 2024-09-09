Hi guys, this is my solution for pento's challenge. 

first i want you to know the brief analysis that i did in this data, first i saw that all files are encoded in jpg/jpeg format in which i had no problem with channels, about resolution i saw that there are different resolutions so i rescaled all the images to 255,255 which
i tought was big enough. I also noticed that we had 80 images, 20 per class which is not a really big number of examples, so i knew that i had to use techniques of data augmentation and/or transfer learning from another
pretrained model to get that low-level understanding of images, so i decided to use mobilenet v2 because it is really lightweight and effective as a first approach.

I split the data into 60% training, 20% validation and 20% test, i think that this distribution of data is fine but it could be different.

I implemented the model using just mobile net v2 and a clasiffier at top of it like if mobile net was just like an embedding, i was thinking to also retrain the last layers of mobile net but accuracy achived 1 in training, 
validation and test sets so it wasn't really necessary and of corse this results are free of overfit, underfit and other common problems for this dataset.

I recommend to upload the jupyter notebook of this repo to drive and open it in google colab, after that follow the instructions in the notebook to run it and provide the necessary data
