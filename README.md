# Near Real-Time Automated Classification of Seismic Signals of Slope Failures with Continuous Random Forests

**Jupyter notebook containing training of classifier and visulalisation used in Wenner et al., submitted to JGR: Earth surface**

In this project, we implement an automatic signals classifcation at Val Bondasca to detect rockfall events.
The classifier is a Random Forest classifier, that was trained on a hand picked catalog of events.
A 40 secondas window with a 15 seconds overlay will run over the contious seismic data stream at each station
and classify the signals seperately. Afterwards we perform a majority vote with the classified classes on each
station weighted by the probabilty of the classification results.


Seismic data not publically available. Access can be granted by [Geopraevent](https://www.geopraevent.ch/?lang=en)

## Prerequisites

* Create new environement

```
conda create -n bondo python=3.6.7
```

* Activate environment
```
conda activate bondo
```

* Install packages

```
conda install scikit-learn numpy scipy obspy pandas imbalanced-learn
```

```
conda config --add channels conda-forge
```

## File explanation

* Automatic_classification.ipynb contains code to read the feature files and evaluate the classifier
* feature_files_2019 contains unlabeled feature files of 2019 to test the classifier 
* split_feature_files contains train and test feature files with labeled data

