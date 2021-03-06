# CNN training and evaluation
This project is used to recognize ethnicity and gender from EAR. The [Paper](https://github.com/123robi/CNN_training/blob/main/paper.pdf) explains the way the project was created and in the end compares two different datasets (AWE Ear dataset and UTKFace dataset) and the gender and race accuracy of each model.
## Dataset
In order to run training model, you have to download following [Dataset.](http://awe.fri.uni-lj.si/datasets.html) In case you don't have premission to do so, feel free to use any other biometric dataset intended for recognition dataset that has annotations that you want to train on.
## Install required requirements
First run `pip install -r requirements.txt`
## CNN Training
- Run `python train.py`

This saves your model to ˙mode.h5`. The model is now ready to use in our prediciton python script.

## Predict
- Load your images or choose the one that is already uploaded to the root directory (`test.png`)
- Run `python predict.py`

This saves the image in `/results` with the corresponding gender and ethnicity information

To run prediction on the half of each database run `python predict_new.py` that runs prediciton on the both databases adn returns accuracy. This may take a while. However, you must first generate corresponding models, and save them to model.h5 and AWEdataset.h5

## Results on training set
Running at `epochs=100`:
- gender accuracy: 99%
- ethnicity accuracy: 94%
-----
## Results on testing set
AWE dataset
- gender accuracy: 64%
- ethnicity accuracy: 55%

UKTFace dataset
- gender accuracy: 38%
- ethnicity accuracy: 52%
## Dataset comparison based on training set
To get the plots run `python plots/plots.py {AWE/UTKFace}.csv`
### UTKFace dataset
![alt text](https://github.com/123robi/CNN_training/blob/main/plots/UTKPlot.png?raw=true)

### AWE Ear dataset
![alt text](https://github.com/123robi/CNN_training/blob/main/plots/AWEplot.png?raw=true)


## Example outputs
![alt text](https://github.com/123robi/CNN_training/blob/main/results/man_asian.png?raw=true)
![alt text](https://github.com/123robi/CNN_training/blob/main/results/south_american.png?raw=true)
