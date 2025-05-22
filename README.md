# Implementing OCR from scratch using K Nearest Neighbours

The training set, i.e., the images and labels of the numbers we want to identify, is obtained from the [MNIST Database](http://yann.lecun.com/exdb/mnist/)

The files in this link often prove troublesome to download, so use Wayback Machine to access an earlier version of the webpage and download the four files from there

We will be implementing k nearest neighbors. The difference between this algorithm and usual machine learning algorithms is that most machine learning algorithms have a training stage, they learn the separating line and then test it. On the other hand, k nearest neighbors does not have this training step in the beginning, it is a lazy learning algorithm. It trains as we try to figure out the new input.

The data are the images themselves, and the labels are the true values of the digits themselves

<img width="368" alt="1" src="https://github.com/user-attachments/assets/b07d7c24-5512-441b-89d6-ff632b6b7415" />

The magic number indicates the type of file

Convention:
X means dataset, y means labels

<img width="373" alt="2" src="https://github.com/user-attachments/assets/9a6840dc-d73e-47c6-8f9c-dc026c0e580b" />


We need the distance between two points

We calculate the normal Euclidian distance in n dimensional space, where n is the number of features. For this, we need a vector consisting of the features, here, the pixels. But the way we've read the file is to make a list of list of these feature vectors. What we want now is just a list of all pixels.

For a particular point (the testing point), k nearest neighbors looks at every other point and calculates the distance, then it takes the point with smallest distance.

k is called a 'hyper parameter', which means it's a number that we can change as per our wish to affect the algorithm such that we can make the output of the algorithm more precise.
