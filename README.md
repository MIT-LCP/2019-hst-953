# hst-953-2019

## Data Access

Participants of the Datathon are added to the Google Group `hst-953-2019`. Members of this group have access to computation resources through the Google Cloud Platform (GCP) project `hst-953-2019` and to datasets via the GCP project `physionet-data`.

You can access the datasets directly on GCP:
1. [Create a free account on GCP](cloud.google.com)
2. [Open `hst-953-2019` in the console](https://console.cloud.google.com/home/dashboard?project=hst-953-2019)
3. [Open BigQuery](https://console.cloud.google.com/bigquery?project=hst-953-2019)
4. Run a query. E.g. count the number of hospital admissions:

   ```SQL
   SELECT count(*)
   FROM `physionet-data.mimiciii_clinical.admissions` 
   ```

## Tutorial Notebooks

You can open the following tutorial notebooks on Colab and get started instantly. Requirements for these notebooks are: (1) you have a Google account, and (2) your Google account has been added to the `hst-953-2019` Google group.

### eICU-CRD
* [01-accessing-the-data.ipynb](https://colab.research.google.com/github/MIT-LCP/2019-hst-953/blob/master/tutorials/eicu/01-accessing-the-data.ipynb)
* [02-explore-patients.ipynb](https://colab.research.google.com/github/MIT-LCP/2019-hst-953/blob/master/tutorials/eicu/02-explore-patients.ipynb)
* [03-severity-of-illness.ipynb](https://colab.research.google.com/github/MIT-LCP/2019-hst-953/blob/master/tutorials/eicu/03-severity-of-illness.ipynb)
* [04-summary-statistics.ipynb](https://colab.research.google.com/github/MIT-LCP/2019-hst-953/blob/master/tutorials/eicu/04-summary-statistics.ipynb)
* [05-prediction.ipynb](https://colab.research.google.com/github/MIT-LCP/2019-hst-953/blob/master/tutorials/eicu/05-prediction.ipynb)

### MIMIC-III
* [mimic-iii-tutorial.ipynb](https://colab.research.google.com/github/MIT-LCP/2019-hst-953/blob/master/tutorials/mimic-iii/mimic-iii-tutorial.ipynb)

### MIMIC-CXR
* [mimic-cxr-train.ipynb](https://colab.research.google.com/github/MIT-LCP/2019-hst-953/blob/master/tutorials/mimic-cxr/mimic-cxr-train.ipynb)

## R 

Datasets can also be queried directly from R. This is exemplified in the following R markdown notebook: [mimic-iii-los.Rmd](https://colab.research.google.com/github/MIT-LCP/2019-hst-953/blob/master/tutorials/mimic-iii/mimic-iii-los.Rmd)

## Accessing MIMIC-CXR

The dataset used in the MIMIC-CXR tutorial is preprocessed for optimal use with [Tensorflow](https://www.tensorflow.org/). If you use a different library or just want a simpler representation of the data, the MIMIC-CXR dataset is available as JPEG images and CSV tables in the following GCP bucket: `gs://physionet-data-mimic-cxr-jpg`. The URL for the bucket is <https://console.cloud.google.com/storage/browser/physionet-data-mimic-cxr-jpg>
