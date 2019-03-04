<div align="right"><b>Name: Hardayal Singh<br>Email: hardayal.msit@gmail.com<br>Batch number: 5</b><br>
<b> Assignment 1C</b>
</div>

<br>

## 1) Convolution
***

In layman terms convolution means combination. It refers to combining 2 matrices to provide an output value or matrix.  In neural networks, image recognition and classification are carried out using Convolution technique.

Consider a grayscale (size 28 X 28 X 1) image showing a single digit number. Our aim is to identify the number. Single digit can be from 0 to 9. Hence, we have 10 possible results.
Every pixel's intensity in the image is represented by a value.

**Note**: In 28 X 28 X1, 1 is the number of channels. It is 1 for grayscale and 3 for RGB images.

![](https://chrisjmccormick.files.wordpress.com/2015/01/layer_1.png)

By rule of thumb, we consider a random 3X3 matrix to slide on this image and extract the features. This results to a layer of 26 X 26. When convoluted again it results in 24 X 24, then 22 X 22 and so on till it reaches 10 X 10 where a well learnt neural network gives the correct output.

- 3 X 3 matrix used here is termed as _'filter'_.
- In the process of convolution when a filter is applied on the input, the result is nothing but sum of dot products of the 2 matrices.


***
## 2) Filters / Kernels
***

Filters are matrices that convolve on an image, used for feature extraction. Consider a single digit number as follows:
 __
 __|
 __|

 We consider 2 **"filters"**  to pull out the features from this image. Horizonal dashes "-" and the vertical ones "|".  Convolution results in:

 Feature Map 1:
  __                        
  __     
  __


Feature Map 2:

|
|

Number of filters is equal to the number of feature maps obtain post convolution.

In CNN, at some point to compress the number of channels we reduce the number of filters and apply point convolution (1 X 1 filter) so as to optimize the model.

***
## 3) 3x3 Convolution
* * *
3 x 3 Convolution is a Feature extractor. In this the filter will keep of size 3 X 3 which appears as 9 pixels of the image, computes an element wise matrix multiplication,do the summation and throw a single number. These filters are used to identify edges, curves from the source image.

Below is an example which shows an effect on size when a 3 X 3 filter is used. A 3 X 3 convolution reduces the input by 2 units (assuming stride =1)
image Size | Filter Size | output Size 
--- | --- | ---
3X3 | 3X3 | 1X1 
4X4 | 3X3 | 2X2
5X5 | 3X3 | 3X3 
6X6 | 3X3 | 4X4 
nXn | 3X3 | n-2 X n-2
#### Example: 3x3 Convolution
![](https://cdn-images-1.medium.com/max/1600/1*EuSjHyyDRPAQUdKCKLTgIQ.png)
![3X3 convolution image](http://static.zybuluo.com/hongchenzimo/q261az03b3cv44q2zcgp4wtb/convolve.png)


***
## 4) Activation Function
***

Activation funciton determine the output of the neural network resulting in a values between (0 and 1) or (-1 and 1) depending upon the function.

### Sigmoid
The sigmoid activation funciton values lies between 0 and 1

![sigmoid curve](https://cdn-images-1.medium.com/max/1600/1*Xu7B5y9gp0iL5ooBj7LtWw.png)
It is used on getting the probablity as an output between the range of 0 and 1. It is a diffrentiable function.On a diffrential of sigmoid we get slope of the curve at any two points on the sigmoid curve.

### Relu Funtion (Rectified Linear unit)
The Relu is much applied on deep learning and convolution neural networks.

![](https://www.safaribooksonline.com/library/view/python-natural-language/9781787121423/assets/02c4f3a4-8c9b-405a-88bd-47b79e3981dc.png)


***
### 5) How to create a repository in Git and basic steps to follow:
***

>#### Create a Repository

  From scratch -- Create a new local repository
  **$ git init [project name]**

  Download from an existing repository
  **$ git clone my_url**

<br>

>#### Observe your Repository
  List new or modified files not yet
  committed
  **$ git status**

  Show the changes to files not yet staged 
  **$ git diff**

  Show the changes to staged files 
  **$ git diff --cached**

  Show all staged and unstaged
  file changes
  **$ git diff HEAD**

  Show the changes between two commit ids
  **$ git diff commit1 commit2**

  List the change dates and authors
  for a file
  **$ git blame [file]**

  Show the file changes for a commit id and/or file
  **$ git show [commit]:[file]**

  Show full change history
  **$ git log**

  Show change history for file/directory including diffs
  **$ git log -p [file/directory]**

<br>

>### Working with Branches

  List all local branches
  **$ git branch**

  List all branches, local and remote 
  **$ git branch -av**

  Switch to a branch, my_branch, and update working directory
  **$ git checkout my_branch**

  Create a new branch called new_branch 
  **$ git branch new_branch**

  Delete the branch called my_branch 
  **$ git branch -d my_branch**

  Merge branch_a into branch_b 
  **$ git checkout branch_b $ git merge branch_a**

  Tag the current commit
  **$ git tag my_tag**

<br>

>#### Make a change

Stages the file, ready for commit 
**$ git add [file]**

Stage all changed files, ready for commit 
**$ git add .**

Commit all staged files to versioned history 
**$ git commit -m “commit message”**

Commit all your tracked files to versioned history
**$ git commit -am “commit message”**

Unstages file, keeping the file changes 
**$ git reset [file]**

Revert everything to the last commit 
**$ git reset --hard**

<br>

>### Synchronize

Get the latest changes from origin (no merge)
**$ git fetch**

Fetch the latest changes from origin and merge
**$ git pull**

Fetch the latest changes from origin and rebase
**$ git pull --rebase**

Push local changes to the origin
**$ git push**

<br>

>### Finally!

When in doubt, use git help
**$ git command --help**

![Git Diagram](https://cdn3.imggmi.com/uploads/2018/5/9/d218367575017f3bd21b368e99e28f12-full.png)