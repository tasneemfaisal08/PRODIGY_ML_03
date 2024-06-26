# PRODIGY_ML_03
Implement a support vector machine (SVM) to classify images of cats and dogs from the Kaggle dataset.

# DATASET 
Kaggle link : https://www.kaggle.com/c/dogs-vs-cats/data

# ABOUT
Using PCA with SVM :
1. High Dimensionality of Image Data
Pixel Features: Each image is represented by its pixel values. For a 50x50 image, this results in 2500 features. Handling such high-dimensional data can be computationally expensive and may lead to issues like overfitting.
Dimensionality Reduction: PCA reduces the number of features by transforming the original high-dimensional space into a lower-dimensional space while retaining most of the variance (information) present in the original data.

2. Improving Computational Efficiency
Training Time: By reducing the number of features, PCA decreases the computational time required for training the SVM model. This is particularly beneficial when working with large datasets or complex models.
Prediction Time: Similarly, prediction times are reduced because the model has fewer features to process.

3. Enhancing Model Performance
Overfitting: High-dimensional data can lead to overfitting, where the model learns noise in the training data instead of the actual signal. PCA helps mitigate this by retaining only the most significant components, effectively filtering out noise.
Generalization: A model trained on a lower-dimensional representation of the data is likely to generalize better to unseen data, leading to improved performance on the test set.

4. Simplifying Hyperparameter Tuning
Pipeline Integration: By integrating PCA into the pipeline, you can perform joint hyperparameter tuning for both PCA and SVM. This ensures that the entire model, including the dimensionality reduction step, is optimized.
Parameter Grid: The param_grid includes pca__n_components, allowing the grid search to find the optimal number of principal components that maximize model performance.
