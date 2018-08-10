
DISCLAIMER: This application is used for demonstrative and illustrative purposes only and does not constitute an offering that has gone through regulatory review.

# Programming Language Classification with IBM Watson Studio, Watson, and GitHub

## Description
In this Code Pattern, we will use Jupyter Notebooks in IBM Watson Studio to build a model that predicts a code's programming language based on its text. The model will then be evaluated against IBM's Watson Natural Languauge classifier.

When the reader has completed this Code Pattern, they will understand how to:

Build a labeled data set
Build a predictive model within a Jupyter Notebook
Configure and use Watson APIs

![](images/architecture.png)

## Flow
1. The developer creates an IBM Watson Studio Workspace.
2. Watson Studio depends on an Apache Spark service.
3. IBM Data Science Experience uses Cloud Object storage to manage your data.
4. This lab is built around a Jupyter Notebook, this is where the developer will gather data, train, and evaluate their model.
5. Create GitHub dataset.
6. Build Naive Bayes Classifier
7. Configure Watson Natural Language Understanding
8. Evaluate Models


## Included components
* [Watson Studio](https://www.ibm.com/bs-en/marketplace/data-science-experience): Analyze data using RStudio, Jupyter, and Python in a configured, collaborative environment that includes IBM value-adds, such as managed Spark.
* [Jupyter Notebook](http://jupyter.org/): An open source web application that allows you to create and share documents that contain live code, equations, visualizations, and explanatory text.
* [Watson Natural Language Classifier](https://www.ibm.com/watson/services/natural-language-classifier/): Understand the intent behind text passages though custom classifiers, complete with a confidence score.

## Featured technologies
* [Watson APIs](https://www.ibm.com/watson/developer/): Watson on the IBM Cloud allows you to integrate the world's most powerful AI into your application and store, train and manage your data in the most secure cloud.
* [Machine Learning](https://medium.com/ibm-data-science-experience): Machine Learning can be applied to disparate solution spaces to deliver disruptive technologies.

# Watch the Video
TBD

# Steps
1. [Create an instance of the IBM Watson Studio Service](#1-create-an-instance-of-the-watson-studio-service)
2. [Create a project in Watson Studio](#2-create-a-project-in-watson-studio-and-bind-it-to-your-watson-machine-learning-service-instance)
3. [Create a notebook in Watson Studio](#3-create-a-notebook-in-watson-studio)
4. [Run the notebooks in Watson Studio](#4-run-the-notebook-in-watson-studio)


### 1. Create an instance of the IBM Watson Studio Service

* In your browser go to the IBM Cloud Dashboard and click `Catalog`.

* Search for and select `Watson Studio`.

  ![](images/dsx-service.jpg?raw=true)

* Verify the service being created is under the Lite plan.

  ![](images/dsx-create.jpg?raw=true)

* Click `Create`

### 3. Create a project in Watson Studio

* In a new browser tab go to [https://datascience.ibm.com](https://datascience.ibm.com).

* Click on `Sign In` at the top of the page.

* From the dashboard, click on `New Project` from the dashboard, select a `Complete` project.

  ![](images/new-project.png?raw=true)

* Projects depend on two services: Object Storage, and a Compute Engine.  If you don't already have Object Storage or a Compute Engine, you can create a new instance of each service while defining a new project.  The _New Project_ panel is easy to use, either select an existing service on the right, or create a new one.  In the example below services need to be created.

  ![](images/create-services.png?raw=true)

> Note: Services created must be in the same region, and space, as your Watson Studio service.

### 4. Create a notebook in Watson Studio

* If you don't have your newly created Project open, first click `Projects` -> `View All Projects`, and then select your newly created project from Step 4. Next, in the Watson Studio browser tab click on `Overview` and then click `add notebooks`.

  ![](images/add-notebook.png?raw=true)

* Click on `From URL` and name the notebook _Apache Spark integration with Watson ML_.

* Under `Notebook URL` provide the following url: https://github.com/IBM/predictive-model-on-watson-ml/blob/master/demo1.ipynb

  ![](doc/source/images/create-notebook.png?raw=true)

* Click `Create Notebook` to create the new notebook.

### 5. Run the notebook in Watson Studio

* Place your cursor in the first code block in the notebook.
* Click on the `Run` icon to run the code in the cell.

* Move your cursor to each code cell and run the code in it. Read the comments for each cell to understand what the code is doing. **Important** when the code in a cell is still running, the label to the left changes to **In [\*]**:.
  Do **not** continue to the next cell until the code is finished running.

* When you get to the cell that says `Stop here !!!!` insert the username and password that you saved from your Watson Machine Learning instance into the code before running it.

* Continue running each cell until you finish the entire notebook.
