# MelanomaChallenge
A melanoma classifier built for a custom kaggle challenge at Télécom ParisTech.

## Methods used :

### Feature Extraction
In the `MelanomaChallenge.ipynb` file, I extracted 26 features corresponding to colors, borders, symmetry and other local features.
Meanwhile, in the `Inception_svm.ipynb` file, the features are obtained by keeping only the convolutional layers of Google's Inception_v3 neural network.

### Oversampling
Since the dataset is highly imbalanced, a resampling gives better results. Due to the small number of samples in the dataset, oversampling is desirable. I chose used the SMOTE implementation from the imbalanced-learn API.

### Dimensionality reduction 
Through Principal Component Analysis and/or Sequential Feature Selection, we can reach a higher score by keeping only the most important features.

### Classifier
I got promising results with Quadratic Discriminant Analyisis and k-Nearest Neighbors. However the most robust classifier is by far a linear SVM. I used the implementations from sklearn for these classifiers.


## Sources :

  - R. Oliveira, N. Marranghello, A. Pereira, J.M. Tavares. **A computational approach for detecting pigmented skin lesions in macroscopic images**, https://www.sciencedirect.com/science/article/pii/S0957417416302354#bib0020
  - H. Ganster, P. Pinz, R. Rohrer, E. Wildling, M. Binder, H. Kittler. **Automated melanoma recognition**, https://ieeexplore.ieee.org/document/918473/
  - M. Zortea, T. Schopf, K. Thon, M. Geilhufe, K. Hindberg, H. Kirchesch, K. Møllersen, J. Schulz, S.O. Skrøvseth, F. Godtliebsen. **Performance of a dermoscopy-based computer vision system for the diagnosis of pigmented skin lesions compared with visual evaluation by experienced dermatologists**, https://www.sciencedirect.com/science/article/pii/S0933365713001589#bib0005
  - A. Esteva, B. Kuprel, R. Novoa, J. Ko, S. Swetter, H. Blau, S. Thrun. **Dermatologist-level classification of skin cancer with deep neural networks**, http://dx.doi.org/10.1038/nature21056


