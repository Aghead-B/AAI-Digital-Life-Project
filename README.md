# Welcome to the digital life readme, in this file we will explain various things about our project.
- A brief overview of what this project is.
- Install requirements, and a step by step on how to get this project working on colabs.
- Various alternative approaches  we tried, and for one reason or another did not end up pursuing.

# What is project Digital Life?
In this project we use Artificial Intelligence to stimulate creativity in the elderly. We do this in three steps:
Step 1, draw something! Our AI then recognizes it and gives it a label. 
Step 2, generate association. We want a new label that is in the same general area, but not exactly the same. Think flowers and trees, not flowers and concrete. 
Step 3, generate a new image. This image will then be displayed back to the user.

In these steps we hope to help the elderly to become more creative, by giving them related and stimulating images of what
they are drawing. If they draw a flower, out system might display back the image of a tree, and the user can in this way copy it,
or hopefully be inspired to draw the tree themselves.

# Install requirements
This project is tested on two running platforms. The first is jupyter notebook, and the second is colabs. Both of these environments
are tested, but both require a number of things to make them run.

- A fair computer. Since our project uses such technologies as stable diffusion and neural networks, it does require a modern computer to
run it.
- Python 3. This project uses various python libraries, and python itself. Here is a tutorial to set up python on a computer:
https://www.digitalocean.com/community/tutorials/install-python-windows-10
- In the project itself will be a cell of commands (all the way at the top) for pip (a python installer, comes with python after version 3.4). This will include quite a few things, and some might take a few minutes to download and install. Be sure to have a stable internet connection and some spare space on the computer hard-drive. In the case of colab, all that needs to be done is to run the cell. In the case of Jupyter notebook, it might be necessary to install them in the command prompt. Simply type 'cmd' in the windows search bar, and then copy the  commands in the cell one by one. Here is a tutorial on how to install matplotlib, to get a taste for it. https://matplotlib.org/stable/users/installing/index.html

# Things we tried, but did not end up using for one reason or another.

Step 1:

Step 2:
In the second step, our first implementation was gensim's word2vec model. A quite good solution, with one big drawback. It works by converting the word you give it and turning it into a vector. It then downloads a file with other vectored word in it, and gets the words that are closest to the vector of the prompt. You could select how many associated word you wanted, and it was fast, lightweight and easy to use. The one big drawback, and the reason we did not end up using it is because of the downloaded file. It only had some 10.000 vectored words in it, and so the more exotic words could not be found, and so it didn't work. For these reason we stepped over to: CONTINUE HERE (this is all that Robert worked on this step) <-----------------

Step 3:
For the third step, we tried a fair few number of things. In the end we used the model from keras: 
https://keras.io/api/keras_cv/models/stable_diffusion/
But we tried a number of things, from looking into payed stable diffusion options (openIA and Replicate seemed the best options we found) to looking into renting a service to run our own model. Our project ended with a local model of stabel diffusion, but we also looked into alternatives. One such was scribble diffusion, a offshoot of stable diffusion where you supply both a prompt and a scribble to make something that is not only influenced by the prompt, but also by what the user drew. This in particular would be a very good continuation of our project, since in step one we have the original scribble that the user supplied. We did not end up going down this road due to time restraint. Should a further team work on this project, scribble diffusion is our recommendation to continue.
