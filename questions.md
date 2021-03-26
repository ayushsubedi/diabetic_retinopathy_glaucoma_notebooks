### Summary
1. We have data from APTOS and IPACS merged together from https://www.kaggle.com/benjaminwarner/resized-2015-2019-blindness-detection-images Each image has been resized and cropped to have a maximum size of 1024px.
2. The data is still noisy. 
3. After balancing the datasets for each class to have the same number of images, we have a total of 2209 in for each class.
4. 20% of this is reserved for validation. Therefore, to train we have ~1765 for each class.
5. The dataset is on drive and we are using colab. 
6. After experimenting with a bunch of transfer learning architecture, we received the best results from:
- Inception v3
- Fine Tuning the entire model
- using ben graham's kaggle winning data augmentation technique
- cropping to remove the black edges
- augmentation (horizontal flip, rotation, normalization)
- val accuracy 55%

### Questions:
1. what is the accuracy that we can target? Is that even a right metric here? 55% accuracy has a "decent" confusion matrix.
2. is one of the issue combining two different datasets, and performing the same augmentation on them?
3. should we look into cleaning the training datasets? removing datasets that have poor quality overall, and/or confusing ones? 
Apart from doing it manually, what might be the right way?
4. normally feature extraction should work but did not in this case, we had to fine tune the whole model. is this expected?
5. should we add more layers on the classifier?
6. how should we prepare when cheers dataset is also added? should that be part of the process from the starting?
7. 
