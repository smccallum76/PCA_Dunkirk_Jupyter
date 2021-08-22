# Dunkirk Critical Minerals Project: PCA Walkthrough

The purpose of this Jupyter Notebook is to provide code based example of the principal components analysis (PCA) applied to the existing Dunkirk dataset.  This example represents an edited version of the full analysis found on the Wildlands Research [statistics dashboard](https://dunkirk-cm.herokuapp.com/pca).

There are two methods for running the notebook, using [Google Colab](https://colab.research.google.com) or using [Jupyter Notebook](https://jupyter.org/).  The easiest of the two methods is to use Google Colab as this method does not require the user to install Jupyter or to load dependencies.  Both methods will be described below.

## Run Notebook using Google Colab (recommended)

The steps for viewing and running the notebook using Colab are as follows:
1. Navigate to Google Colab: https://colab.research.google.com.
2. Colab should show a notebook loading window that provides options Examples, Recent, Google Drive, GitHub, and Upload.  If this screen does not automatically appear, then select **File** and then **Open Notebook**. 
3. From the notebook loading window select **GitHub** and then copy and paste the following URL into the field labeled **Enter a GitHub URL or search by organization or user**. https://github.com/smccallum76/PCA_Dunkirk_Jupyter
4. From here two files should be visible, select the file **Dunkirk_PCA_colab.ipynb**, which will load the Notebook into Colab.  

Colab provides a Python environment that is preloaded with most of the common Python libraries.  However, this example requires the use of a library called *jupyter_dash*, which is not preloaded within Colab.  For this reason the first line of code in the PCA Notebook is a ```!pip install jupyter_dash```, which must be executed when first running the code in Colab.  

