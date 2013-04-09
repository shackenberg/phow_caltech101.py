phow_caltech101.py
==================

Simple example script for content based image classification using the bag of visual words approach. 

The scritp is based on [phow_caltech101.m][1], a 'one file' example script using the [VLFeat library][6] to train an test an image classifier on the [Caltech-101 data set][4]. 

This Python version archives the same average accuracy of around 65% using as the original file: 

- PHOW features (dense multi-scale SIFT descriptors)
- Elkan k-means for fast visual word dictionary construction
- Spatial histograms as image descriptors
- A homogeneous kernel map to transform a Chi2 support vector machine (SVM) into a linear one
- Liblinear SVM (instead of the Pegasos SVM of the Matlab script)

The code also works with other datasets if the images are organized like in the Calltech data set, where all images belonging to one class are in the same folder:
    
    .
    |-- path_to_folders_with_images
    |    |-- class1
    |    |-- class2
    |    |-- class3
    ...
    |    └-- classN

Requisite:

- [VLFeat with a Python wrapper][2]
- [scikit-learn][5] for VLFeat functions that don't have a Python wrapper yet. 
- [The Caltech101 dataset][3]

[5]: http://scikit-learn.org/stable/
[4]: http://www.vision.caltech.edu/Image_Datasets/Caltech101/
[2]: https://pypi.python.org/pypi/pyvlfeat/0.1.1a3
[3]: http://www.vision.caltech.edu/Image_Datasets/Caltech101/101_ObjectCategories.tar.gz
[1]: http://www.vlfeat.org/applications/caltech-101-code.html
[6]: http://www.vlfeat.org/index.html
