# Concordia University

Department of Computer Science and Software Engineering COMP 6721

APPLIED ARTIFICIAL INTELLIGENCE

Project

## Group J

## Authors

Name: Jatin Arora 
Applicant ID: 40225129

Name: Rahul Singh 
Applicant ID: 40228461

Name: Devanshi Patel 
Applicant ID: 40172139

Name: Reva Balasundaram 
Applicant ID: 40227644

## High Level Description of Project
Facial image recognition refers to the use of computer algorithms to analyze and identify emotions displayed on a person's face.This report explores the problem of facial emotion recognition through deep learning using Convolutional Neural Networks (CNNs). The aim is to classify emotions from facial features such as the position and shape of the mouth, eyes, and eyebrows. Three datasets from Kaggle were selected, ensuring they had enough and different number of classes and images to train the model effectively. The MobileNet v2, ShuffleNet v2, and ResNet 18 architectures were trained on all three datasets and then used to analyze how the combinations of different hyperparameters and models impact the accuracy of facial emotion recognition. ResNet18 resulted as the best model for all three datasets, performing the highest in terms of accuracy and F1-score. FER2013 dataset had the best results overall, likely due to its smaller dataset size and balanced data. MobileNetV2 outperformed ResNet18 and ShuffleNetV2 on FER2013, while ResNet18 achieved the highest accuracy on AffectNetHQ and the Tiny dataset. Lastly in the ablation study, the impact of different hyperparameters on model performance was analyzed. It was found that changing the number of classes for training, the number of images per class, and the learning rate had a significant impact on model performance.

## Requirements to run the code
matplotlib         &nbsp;&nbsp;&nbsp;&nbsp; 3.7.1  <br/>
numpy              &nbsp;&nbsp;&nbsp;&nbsp; 1.22.4  <br/>
seaborn            &nbsp;&nbsp;&nbsp;&nbsp; 0.12.2  <br/>
session_info       &nbsp;&nbsp;&nbsp;&nbsp; 1.0.0  <br/>
sklearn            &nbsp;&nbsp;&nbsp;&nbsp; 1.2.2  <br/>
torch              &nbsp;&nbsp;&nbsp;&nbsp; 1.13.1+cu116  <br/>
torchvision        &nbsp;&nbsp;&nbsp;&nbsp; 0.14.1+cu116  <br/>
tqdm               &nbsp;&nbsp;&nbsp;&nbsp; 4.65.0  <br/>
<br/>
<br/>
IPython            &nbsp;&nbsp;&nbsp;&nbsp; 7.9.0  <br/>
jupyter_client     &nbsp;&nbsp;&nbsp;&nbsp; 6.1.12  <br/>
jupyter_core       &nbsp;&nbsp;&nbsp;&nbsp; 5.3.0  <br/>
notebook           &nbsp;&nbsp;&nbsp;&nbsp; 6.5.3  <br/>

## Instruction on how to train/validate the model
```
> Clone the repo
    >> git clone https://github.com/jatin51997/AI-Project.git
> Upload the Ipython notebooks on google colab/Kaggle.
> Upload the datasets from the given google drive link and modify the datasets paths in the notebooks accordingly. For example:
    train_dir = '/kaggle/input/'+data+'/train/'
    val_dir = '/kaggle/input/'+data+'/validation/'
    test_dir ='/kaggle/input/'+data+'/test/'
> The notebooks are now ready to run!
```

## Instructions on how to run the pre-trained model on the provided sample test dataset
```
Saved Models:
    https://drive.google.com/file/d/1NHC3PanLMn3A3MntDgFh5Trpv-6UGzfR/view?usp=share_link
Sample Datasets:
    https://drive.google.com/file/d/1CvSK1C6NOLSs4onHDoRYaxOgPjmgLf3y/view

> Use the TestModelOnSample.ipynb file to run the models on sample dataset.
> Modify the paths for the model and the dataset, point to the test folder of the dataset as below:
    datasetPath = '/kaggle/input/fer2013/FER2013/test/'
    modelPath = '/kaggle/input/sample2/TL_resnet18_FER2013.pth'
```

##Source Code Package In PyTorch
1)9models.ipynb: This file contains the code for training, validating and testing the 9 models.
2)TransferLearning.ipynb: This file contains the code for 2 transfer learning models.
3)HyperparameterOptimisation.ipynb: This file contains the code for Hyperparameter Optimisation of 1 model.
4)Preprocessing.ipynb: This file contains the code used to preprocess the datasets.
5)TestModelOnSample.ipynb: This file contains the code to test the sample dataset using the saved models that were trained earlier.

## Description on how to obtain the Dataset 

Original Datasets:
1) FER-tiny: https://www.kaggle.com/datasets/sakuraisana/facial-emotion-recognition-tiny?select=validation
2) Affectnethq: https://www.kaggle.com/datasets/tom99763/affectnethq
3) FER2013: https://www.kaggle.com/datasets/msambare/fer2013

Modified Datasets After Preprocessing:
https://drive.google.com/file/d/1Gmd3cbTFohimCey-1DJUWAOFJk5twf_s/view

Sample Dataset:
https://drive.google.com/file/d/1CvSK1C6NOLSs4onHDoRYaxOgPjmgLf3y/view


