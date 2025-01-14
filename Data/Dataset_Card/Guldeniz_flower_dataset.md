#flowersdataset #segmentation #VGG

# Dataset Card for Flowers Dataset

## Table of Contents
- [Dataset Description](#dataset-description)
  - [Dataset Summary](#dataset-summary)
  - [Official VGG'S README.md](#official-vggs-README.md)

## Dataset Description

- **Homepage:** https://www.robots.ox.ac.uk/~vgg/data/flowers/17/index.html
- **Repository:** https://huggingface.co/datasets/Guldeniz/flower_dataset
- **Paper:** [Needs More Information]
- **Leaderboard:** [Needs More Information]
- **Point of Contact:** [Needs More Information]

### Dataset Summary

VGG have created a 17 category flower dataset with 80 images for each class. The flowers chosen are some common flowers in the UK. The images have large scale, pose and light variations and there are also classes with large varations of images within the class and close similarity to other classes. The categories can be seen in the figure below. We randomly split the dataset into 3 different training, validation and test sets. A subset of the images have been groundtruth labelled for segmentation.
You can find the split files in the link, as a mat file.

### Official VGG's README.md

17 Flower Category Database
----------------------------------------------
This set contains images of flowers belonging to 17 different categories. 
The images were acquired by searching the web and taking pictures. There are
80 images for each category. 

The database was used in:

Nilsback, M-E. and Zisserman, A.  A Visual Vocabulary for Flower Classification.
Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (2006) 
http://www.robots.ox.ac.uk/~vgg/publications/papers/nilsback06.{pdf,ps.gz}.

The datasplits used in this paper are specified in datasplits.mat

There are 3 separate splits. The results in the paper are averaged over the 3 splits.
Each split has a training file (trn1,trn2,trn3), a validation file (val1, val2, val3)
and a testfile (tst1, tst2 or tst3). 

Segmentation Ground Truth
------------------------------------------------
The ground truth is given for a subset of the images from 13 different
categories. 

More details can be found in:

Nilsback, M-E. and Zisserman, A. Delving into the whorl of flower segmentation.
Proceedings of the British Machine Vision Conference (2007)
http:www.robots.ox.ac.uk/~vgg/publications/papers/nilsback06.(pdf,ps.gz).

The ground truth file also contains the file imlist.mat, which indicated
which images in the original database that have been anotated.

Distance matrices
-----------------------------------------------

We provide two set of distance matrices:

1. distancematrices17gcfeat06.mat 
- Distance matrices using the same features and segmentation as detailed in:
    Nilsback, M-E. and Zisserman, A.  A Visual Vocabulary for Flower Classification.
    Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition(2006)
    http://www.robots.ox.ac.uk/~vgg/publications/papers/nilsback06.{pdf,ps.gz}.

2. distancematrices17itfeat08.mat
- Distance matrices using the same features as described in: 
    Nilsback, M-E. and Zisserman, A. Automated flower classification over a large number of classes.
    Proceedings of the Indian Conference on Computer Vision, Graphics and Image Processing (2008)
    http://www.robots.ox.ac.uk/~vgg/publications/papers/nilsback08.{pdf,ps.gz}.
  and the iterative segmenation scheme detailed in 
    Nilsback, M-E. and Zisserman, A. Delving into the whorl of flower segmentation.
    Proceedings of the British Machine Vision Conference (2007)
    http:www.robots.ox.ac.uk/~vgg/publications/papers/nilsback06.(pdf,ps.gz).