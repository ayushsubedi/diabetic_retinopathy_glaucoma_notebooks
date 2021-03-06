
# README

## Glaucoma Prediction
![](https://www.inmedpharma.com/wp-content/uploads/2020/05/Glaucoma-compared-to-normal-vision.png)

Glaucoma is a common eye condition where the optic nerve, which connects the eye to the brain, becomes damaged. It's usually caused by fluid building up in the front part of the eye, which increases pressure inside the eye. Glaucoma can lead to loss of vision if it's not diagnosed and treated early.

### TODOS

## What worked? (90% accuracy)
1. densenet sequential with ben on himanchu dataset, using NLLLoss criterion, Adam optimizer 

## Limitation
1. very much dependent on dataset
2. disk extraction is good but is very subjective to the dataset
3. trained on very small dataset  

## Preliminary
- [x] create a gmail account (glaucomadetection@gmail.com)
- [x] understand the difference between possibility of glaucoma by classification (vs measurements)

## Preprocessing
- [x] ben transformation
- [x] extract disk from fundus images
- [x] improve extraction algorithms 
- [x] perform EDA on disk image to find troubling images (cases where crop does not work)
- [x] convert python function to extract disk to torch transform class (failed)
- [x] transformation to disk during training failed. create a disk dataset before training the model.
- [x] train on new dataset with and without ben transformation
- [x] handle imbalanced class with class weighting
- [x] convert Kaggle dataset to the format that we have templated our notebooks with
- [x] for kaggle dataset get disks using new algorithm


## Obseverations in regards to disk generation
- extraction of disk does not help (too many vague areas left unfilled)
- however, cropping shows very good promise
- but, cropping requires somewhat similar of fundus images
 

## Datasets
- [x] find datasets https://deepblue.lib.umich.edu/data/concern/data_sets/3b591905z, https://www.kaggle.com/andrewmvd/ocular-disease-recognition-odir5k
- [x] create a dataset from Magrabia
- [x] create a dataset from Messidor
- [x] create a dataset from Ocular Disease Recognition
- [x] create EDA on non measurement dataset (Ocular Disease Recognition)
- [x] create a dataset from ocular disease recognition to include normal and glaucoma images
- [x] (Kaggle dataset, custom generated, filtered)https://www.kaggle.com/sshikamaru/glaucoma-detection?select=glaucoma.csv
- [x] train on Kaggle dataset (without changing anything)


## Training
- [x] inception v3 with and without ben on ocular, kaggle, and himanchu dataset
- [x] inception v3 with ben on ocular, kaggle, and himanchu dataset (disk extracted, normal, and cropped dataset)
- [x] densenet linear with ben on ocular, kaggle, and himanchu dataset 
- [x] densenet linear with ben on ocular, kaggle, and himanchu dataset (disk extracted, normal, and cropped dataset)
- [x] densenet sequential with ben on ocular, kaggle, and himanchu dataset 
- [x] densenet sequential with ben on ocular, kaggle, and himanchu dataset (disk extracted, normal, and cropped dataset)
- [x] add datasets from cheers for testing
- [x] add datasets from cheers for training


## Diabetic Retinopathy Prediction
![](https://gadsdeneye.com/wp-content/uploads/diabetic-retinopathy-vector.jpg)

Diabetic retinopathy is a complication of diabetes, caused by high blood sugar levels damaging the back of the eye (retina). It can cause blindness if left undiagnosed and untreated. However, it usually takes several years for diabetic retinopathy to reach a stage where it could threaten your sight.


## What worked? (90% accuracy)
1. Large dataset from EyePACS (Kaggle competition used training (30%) and testing data (70%) from Kaggle. After the competition, the labels were published). Flipped the ratios for our use case. 
2. Remove out of focus images
3. Remove too bright, and too dark images.
4. Link to clean dataset https://www.kaggle.com/ayushsubedi/drunstratified
5. To handle class imbalanced issue, used weighted random samplers. Undersampling to match no of images in the least class (4) did not work. Pickled weights for future use.
6. Ben Graham transformation and augmentations
7. Inception v3 fine tuning, with aux logits trained (better results compared to other architecture)
8. Perform EDA on inference to observe what images were causing issues
9. Removed the images and created another dataset (Link to the new dataset https://www.kaggle.com/ayushsubedi/cleannonstratifieddiabeticretinopathy
10. See 5, 6, and 7


### TODOS

### Datasets
Binary Stratified (cleaned): https://drive.google.com/drive/folders/12-60Gm7c_TMu1rhnMhSZjrkSqqAuSsQf?usp=sharing
Categorical Stratified (cleaned): https://drive.google.com/drive/folders/1-A_Mx9GdeUwCd03TUxUS3vwcutQHFFSM?usp=sharing
Non Stratified (cleaned): https://www.kaggle.com/ayushsubedi/drunstratified
Recleaned Non Stratified: https://www.kaggle.com/ayushsubedi/cleannonstratifieddiabeticretinopathy



#### Priliminary
- [x] create a new gmail account to store datasets (diabeticretinopathyglaucoma@gmail.com)
- [x] https://www.youtube.com/watch?v=VIrkurR446s&ab_channel=khanacademymedicine What is diabetic retinopathy?
- [x] collect all previous analysis notebooks
- [x] conduct preliminary EDA (for balanced dataset, missing images etc)
- [x] create balanced test train split for DR (stratify) 
- [x] store the dataset in drive for colab
- [x] identify a few research papers, create a file to store subsequently found research papers
- [x] identify right technology stack to use (for ML, training, PM, model versioning, stage deployment, actual deployment)
- [x] perform basic augmentation
- [x] create a version 0 base model
- [x] apply a random transfer learning model 
- [x] create a metric for evaluation
- [x] store the model in zenodo, or find something for version control
- [x] create a model that takes image as an input
- [x] create a streamlit app that reads model
- [x] streamlit app to upload and test prediction
- [x] test deployment to free tier heroku
- [x] identify gaps 
- [x] create priliminary test set
- [x] create folder structures for saved model in the drive
- [x] figure out a way to move files from kaggle to drive (without download/upload)
- [x] research saving model (the frugal way)
- [x] research saving model to google drive after each epoch so that during unforseen interuptions, the training of the model can be continued 

### Resource
- [x] upgrade to 25GB RAM in Google Colab possibly w/ Tesla P100 GPU
- [x] upgrade to Colab Pro

### Baseline
- [x] medicmind grading (accuracy: 0.8)
- [x] medicmind classification (0.47)

#### Transfer Learning
- [x] resnet
- [x] alexnet
- [x] vgg
- [x] squeezenet
- [x] densenet 
- [x] inception
- [x] efficient net

#### Dataset clean images
- [x] create a backup of primary dataset (zip so that kaggle kernels can consume them too)
- [x] find algorithms to detect black/out of focus images
- [x] identify correct threshold for dark and out of focus images
- [x] remove black images
- [x] remove out of focus images 
- [x] create a stratified dataset with 2015 data only (convert train and test both to train and use), remove black images and out of focus images (also create test set)
- [x] create non-stratified dataset with 2015 clean data only (train, test, valid) (upload in kaggle if google drive full)
- [x] create a binary dataset (train, test, valid)
- [x] create confusion matrices (train, test, valid) after clean up (dark and blurry)
- [x] the model is confusing labels 0 and 1 as 2, is this due to disturbance in image in 0. 
- [x] concluded that the result is due to the model not capturing class 0 enough (due to undersampling)

#### Inference
- [x] create a csv with preds probability and real label
- [x] calculate recall, precision, accuracy, confusion matrix
- [x] identify different prediction issues
- [x] relationship between difference in preds and accuracy
- [x] inference issue: labels 0 being predicted as 4
- [x] inference issue: Check images from Grade 2, 3 being predicted as Grade 0
- [x] inference issue: Check images from Grade 4 being predicted as Grade 0
- [x] inference issue: Check images from Grade 0 being predicted as Grade 4
- [x] inference issue: A significant Grade 2 is being predicted as Grade 0
- [x] inference issue: More than 50% of Grade 1 is being predicted as Grade 0
- [x] create a new dataset


#### Model Improvement
- [x] research kaggle winning augmentation for DR
- [x] research appropriate augmentation: optical distortion, grid distortion, piecewise affine transform, horizontal flip, vertical flip, random rotation, random shift, random scale, a shift of RGB values, random brightness and contrast, additive Gaussian noise, blur, sharpening, embossing, random gamma, and cutout
- [x] train on various pretrained models or research which is supposed to be ideal for this case https://pytorch.org/vision/stable/models.html
- [x] create several neural nets (test different layers)
- [x] experiment with batch size
- [x] Reducing lighting-condition effects
- [x] Cropping uninformative area
- [x] Create custom dataloader based on ben graham kaggle winning strategy
- [x] finetune vs feature extract
- [x] oversample
- [x] undersample
- [x] add specificity and sensitivity to indicators
- [x] create train loss and valid loss charts
- [x] test regression models (treat this as a grading problem)
- [x] pickle weights


#### Additional Models
- [x] check if left/right eye classification model is required

#### Additional datasets
- [x] make datasets more extensive (add test dataset with recoverd labels to train dataset 2015)
- [x] add APTOS dataset 
- [x] request labelled datasets from cheers 
- [ ] add datasets from cheers for testing
- [ ] add datasets from cheers for training

#### Test datasets
- [x] find datasets for testing (dataset apart from APTOS and EyePACS) 
- [x] update folder structures to match our use case
- [x] find dataset for testing after making sure old test datasets are not in vaid/train (4 will be empty)

#### Concepts/Research Papers
- [x] read reports from kaggle competition winning authors 
- [x] Deep Learning Approach to Diabetic Retinopathy Detection https://arxiv.org/pdf/2003.02261.pdf
- [x] Google research https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/45732.pdf
- [x] Nature article https://www.nature.com/articles/s41746-019-0172-3
- [x] read ravi's article
- [x] https://deim.urv.cat/~itaka/itaka2/PDF/acabats/PhD_Thesis/TESI_doctoral_Jordi_De_la_Torre.pdf
- [x] what can go wrong https://yerevann.github.io/2015/08/17/diabetic-retinopathy-detection-contest-what-we-did-wrong/
- [x] https://arxiv.org/pdf/1902.07208.pdf 
- [x] identify more papers



