# Data Science Toolbox 4: (Mis) Identifying Users by Command Usage

This is a group project completed for the "Data Science Toolbox" course at Bristol University. The project brief was to explore neural networks and their application to cyber-security. This project considers how they can be applied to detecting intrusions. We then develop an attack against this solution using an adversarial network. Considering the network we are attacking as a black-box, we build a replica network using carefully chosen points in the sample space. We then examine the internals of this replica to build fake inputs which trick the network. The outcome is a Python function which takes a malicious shell script as input, and outputs an equivelant script that is classified by the intrusion detection system as "legitimate".

The best entrypoint would be to skim our [report](./project/report.pdf), then take a look at the [notebook](./project/report.ipynb) where we implement the intrusion detection and our attack. The Jupyter notebook can be downloaded and run locally, or within Google Colab. See below for more details.

## Running locally
We've frozen our dependencies in `requirements.txt`, so the following should get a local installation up and running:
```
pip install -r requirements.txt
```

## Running with Google Colab
Following [this link](https://colab.research.google.com/github/dj311/data-science-toolbox-5/blob/master/project/report.ipynb) will open the main report in colab. Then run the following in a code cell:

```
!pip install cleverhans
```

(this is commented out in the top code cell). The rest of our requirements come pre-installed.

## Data
We've included a compressed version of the data set in this repo (sourced from http://www.schonlau.net/intrusion.html). However, the code in our notebook will download and unzip the data directly into memory (i.e. the data directory in this repo isn't needed to run the notebook, but an internet connection is).
