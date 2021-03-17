
# README
## Diabetic Retinopathy Prediction
![](https://gadsdeneye.com/wp-content/uploads/diabetic-retinopathy-vector.jpg)

Diabetic retinopathy is a complication of diabetes, caused by high blood sugar levels damaging the back of the eye (retina). It can cause blindness if left undiagnosed and untreated. However, it usually takes several years for diabetic retinopathy to reach a stage where it could threaten your sight.

### TODOS

#### Priliminary
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
- [ ] create test set
- [ ] research saving model (the frugal way)
- [ ] research saving model to google drive after each epoch so that during unforseen interuptions, the training of the model can be continued 


#### Model Improvement
- [ ] research kaggle winning augmentation for DR
- [ ] apply appropriate augmentation
- [ ] train on various pretrained models or research which is supposed to be ideal for this case https://pytorch.org/vision/stable/models.html
- [ ] create several neural nets (test different layers)
- [ ] experiment with batch size
- [ ] create confusion matrices for each training permutation
- [ ] add specificity and sensitivity to indicators
- [ ] create train loss and valid loss charts

#### Additional Models
- [ ] check if left/right eye classification model is required

#### Additional datasets
- [ ] add datasets from cheers for testing
- [ ] add datasets from cheers for training
- [ ] train with png datasets 


#### Concepts/Research Papers
- [ ] read reports from kaggle competition winning authors 
- [ ] Google research https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/45732.pdf
- [ ] Nature article https://www.nature.com/articles/s41746-019-0172-3
- [ ] identify more papers


#### Engineering and Deployment
- [ ] Cheers fundus image has text label for left/right eye. Research on how this impacts ML
- [ ] If there is an impact, how to get around
- [ ] Create flask app
- [ ] Create authentication for interface and API
- [ ] Create a mechanism to store uploaded files
- [ ] Create a mechanism for seemless transitioning when models are updated
- [ ] Add issue trackers
- [ ] Identify more engineering problems
- [ ] Figure out ways to deploy for staging
- [ ] Create table schema
- [ ] Identify patient tracking
- [ ] Create a simple dashboard 


#### User Interface/API
- [ ] Add swagger to the project for API documentation
- [ ] Add Sphinx for project documentation
- [ ] Add bearer authentication for API
- [ ] Provide additional information on the interface and not just the prediction (probability, index, charts etc)
- [ ] Use bulma or tailwind for CSS
- [ ] Identify more UI/API todos


## Glaucoma Prediction
![](https://www.inmedpharma.com/wp-content/uploads/2020/05/Glaucoma-compared-to-normal-vision.png)

Glaucoma is a common eye condition where the optic nerve, which connects the eye to the brain, becomes damaged. It's usually caused by fluid building up in the front part of the eye, which increases pressure inside the eye. Glaucoma can lead to loss of vision if it's not diagnosed and treated early.

### TODOS

- [ ] identify todos 
