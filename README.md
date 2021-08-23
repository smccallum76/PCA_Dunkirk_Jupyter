# Dunkirk Critical Minerals Project: PCA Walkthrough

The purpose of this Jupyter Notebook is to provide a code-based example of the principal components analysis (PCA) applied to the existing Dunkirk X-ray Fluorescence (XRF) dataset.  This example represents an edited version of the full analysis found on the Wildlands Research [statistics dashboard](https://dunkirk-cm.herokuapp.com/pca). 

In an effort to replicate the actual dashboard as closely as possible, a module called JupyterDash was used.  JupyterDash allows the script to be run as though it is a web-based application using the local machine as a server.  This approach does result in a known issue described below.  

There are two methods for running the notebook, using [Google Colab](https://colab.research.google.com) or using [Jupyter Notebook](https://jupyter.org/).  The easiest of the two methods is to use Google Colab as this method does not require the user to install Jupyter or to load dependencies.  Both methods will be described below.

## Run Notebook using Google Colab (recommended)

The steps for viewing and running the notebook using Colab are as follows:
1. Navigate to Google Colab: https://colab.research.google.com.
2. Colab should show a notebook loading window that provides options *Examples, Recent, Google Drive, GitHub,* and *Upload*.  If this screen does not automatically appear, then select **File** and then **Open Notebook**. 
3. From the notebook loading window select **GitHub** and then copy and paste the following URL into the field labeled **Enter a GitHub URL or search by organization or user**. https://github.com/smccallum76/PCA_Dunkirk_Jupyter
4. From here two files should be visible, select the file **Dunkirk_PCA_colab.ipynb**, which will load the Notebook into Colab.  

Colab provides a Python environment that is preloaded with most of the common Python libraries.  However, this example requires the use of a library called *jupyter_dash*, which is not preloaded within Colab.  For this reason the first line of code in the PCA Notebook is a ```!pip install jupyter_dash```, which must be executed when first running the code in Colab.

## Run Notebook using Jupyter Notebook

This notebook was originally developed using Jupyter Notebook.  If this method is selected, then it is assumed the user has experience setting up a virtual environment and loading the dependencies necessary to execute the code.  A **requirements.txt** file is included within this Git repository that can be used to install the necessary modules. The recommended approach when using this method is as follows:
1. Clone this repository locally.
2. Using [Anaconda](https://www.anaconda.com/), or your chosen platform, create a virtual environment, and install the dependencies defined in **requirements.txt**. 
3. Activate this environment (from Anaconda or command line) and open Jupyter Notebooks.
4. Navigate to the cloned repository and open the notebook **Dunkirk_PCA_jupyter.ipynb**.

### One Warning/Known Issue

A known issue, whether using Colab or Jupyter, is that occasionally the ports used when calling ```app.run_server(mode='inline', port=<your_port_number>)``` are not properly deactivated, which will result in a failure to load the visualization.  If this occurs, then two methods can be used to resolve the issue:
1. open a command terminal and type the following (in bold): **npx kill-port 8050**.  Note that "8050" may not be the port number, so please change the number to match the error.  
2. Directly change the port number in the code.  For instance, if port 8050 is problematic, then change the number to 9000, or nearly any number greater than 2000 and less than 10000.  For example, change ```app.run_server(mode='inline', port=8050``` to ```app.run_server(mode='inline', port=9000```)

