# [Apache Spark Intro](https://spark.apache.org/)
* **What is Apache Spark?**

   Apache Spark is an open-source cluster-computing framework(wiki). It is a general-purpose Big data processing engine, suitable for use in a wide range of circumstances. It allows data workers to efficiently execute streaming, machine learning or SQL workloads that require fast iterative access to datasets.  it works with the filesystem to **distribute**  data across the cluster, and process that data in **parallel**. **Spark jobs perform multiple operations consecutively, in memory and only
spilling to disk when required by memory limitations.**
    * [Chapter One](http://www.bigdata-toronto.com/2016/assets/getting_started_with_apache_spark.pdf)
    
* **Why  Apache Spark??**
    * [Spark is mostly popular for its speed,ease of use,capability of running evereywhere ](https://spark.apache.org/) 
    * It is much more faster than MapReduce
    * [Use case](https://hortonworks.com/apache/spark/#section_2)
* **Spark is not the alternative of Hadoop. It is the alternative of MapReduce**
* [Spark Ecosystem](https://www.kdnuggets.com/2016/03/top-spark-ecosystem-projects.html)


![alt text][SparkEcosystem]

# Spark with Python
#### Note: Scala is recomended for Spark, but Python is always good for quick learning. 
* [Python vs Scala](https://www.datacamp.com/community/tutorials/apache-spark-python)
## [Spark with Python Intro](https://www.kdnuggets.com/2015/11/introduction-spark-python.html)

## Installation
* **Requirements**
    * OS - **Linux /Mac / Windows** 
    * **Spark**
    * **Python**
    * **Scala,** **Java**

### Installation Instructions
**Below instructions are applicable for Ubuntu 16.04**
* Here we use **Spark 2.1.0** , for this perticular version we need to install **Python3.5** to avoid any issue.
* First we have to check the default Python version, to do this, open **Terminal** any run:
    * **$ python3**
         * if the version is 3.5 then it's ok, otherwise install Python3.5
* Install pip3
    * **$ sudo apt install python-3 pip**
* Install **jupyter notebook**
    * **$ pip3 install jupyter**
    * **$ jypyter notebook**
    * it will open jupyter notebook in our default browser, if it is not opend then click the link from **terminal**

![alt text][jupyterNotebook]

* Now we nedd **JAVA**. First check if it exists:
    * **$ java -version**
    * if it is preinstalled it will show something like this "openjdk version "1.8.0_151....etc""
* If not installed previously:
    * **$ sudo apt-get update**
    * **$ sudo apt-get install default-jre**
    * **$ java -version**

* Now install **Scala**
    * **$ sudo apt-get install scala**
    * **$ scala -version**

* To connect python with scala and java we need to install **py4j**
    * **$ pip3 install py4j**
### Now its time to install **Spark**
*   To download spark visit this link : https://spark.apache.org/downloads.html and set 
**spark release : 2.1.0** and **package type:Pre-built Hadoop 2.7 and later** like following image 

![alt text][sparkDownload]



* Now click to download "Download Spark: spark-2.1.0-bin-hadoop2.7.tgz"
* After finishing download cut-paste **spark-2.1.0-bin-hadoop2.7.tgz to** **"home"** directory
    * goto **"home"** directory and open "terminal" and run following commands:
         * **$ sudo tar -zxvf spark-2.1.0-bin-hadoop2.7.tgz**
         * **$ export SPARK_HOME='home/asif/spark-2.1.0-bin-hadoop2.7'**
            * write this path "home/asif/spark-2.1.0-bin-hadoop2.7" according to your pc  
         * **$ export PATH=$SPARK_HOME:$PATH**
         * **$ export PYTHONPATH=$SPARK_HOME/python:$PYTHONPATH**
         * **$ export PYSPARK_DRIVER_PYTHON="jupyter"**
         * **$ export PYSPARK_DRIVER_PYTHON_OPTS="notebook"**
         * **$ export PYSPARK_PYTHON=python3**
         * **$ sudo chmod 777 spark-2.1.0-bin-hadoop2.7**
         * **$ cd spark-2.1.0-bin-hadoop2.7/**
         * **$ cd python**
         * **$ python3**
         * Last command will open python editor, type there "**import pyspark**" if it runs without error, then we are done!!
         * Now type "**quit()**" to get out......
 * if the above installation doesnt work and Python3.6 or other version with anaconda is preinstalled in the system, there are few more steps to go. In the terminal run following commands:
    * **$ export PATH=~/anaconda3/bin:$PATH**
    * **$ conda create -n py35 python=3.5 anaconda**
        * 'py35' is the name of the environment
    * To activate this Python3.5 env:
        * **$ source activate py35**
        * **$ python3**
        * **import pyspark** # it should work fine now
        * **quit()**
    * To deactivate :
        * **source deactivate**

## Getting Started

* Open terminal , and run following commands to open **jupyter notebook**
    * **$ ls**
    * **$ cd spark-2.1.0-bin-hadoop2.7**
    * **$ cd python**
    * **$ jupyter notebook**
    

* [DataFrame, Cleaning Data & Spark Sql Code Example](https://github.com/Shayokh144/Spark_with_Python/tree/master/DataFrameAndCleaningData)
* [Spark MLlib Code Example](https://github.com/Shayokh144/Spark_with_Python/tree/master/MLlib)
    * [Linear Regression](https://github.com/Shayokh144/Spark_with_Python/blob/master/MLlib/Linear_Regression_example.ipynb)
    * [Logistic Regression](https://github.com/Shayokh144/Spark_with_Python/blob/master/MLlib/LogisticRegressionExample.ipynb)
    * [Tree Regression](https://github.com/Shayokh144/Spark_with_Python/blob/master/MLlib/TreeRegressionExample.ipynb)
    * [Classifier Tree](https://github.com/Shayokh144/Spark_with_Python/blob/master/MLlib/TreeFamilyExample.ipynb)
    * [Recommendation System(Collaborative Filtering)](https://github.com/Shayokh144/Spark_with_Python/blob/master/MLlib/MovieRecomendation(Collaborative%20Filtering).ipynb)
    * [Multilayer Perceptron (in Binary classification)](https://github.com/Shayokh144/Spark_with_Python/blob/master/MLlib/MultilayerPerceptronClassifier.ipynb)
    * [Multilayer Perceptron (in Multiple classification)](https://github.com/Shayokh144/Spark_with_Python/blob/master/MLlib/MultilayerPerceptron(SeedData).ipynb)
    * [Unsupervised(K-means)](https://github.com/Shayokh144/Spark_with_Python/blob/master/MLlib/ClusteringOnSeedData.ipynb)
* [Hypermeter Tuning with cross validation and train validation split](https://github.com/Shayokh144/Spark_with_Python/blob/master/HyperparameterTuning/HyperparameterTuningExample.ipynb)
* [Spark MLlib Doc](https://spark.apache.org/docs/2.1.0/ml-guide.html)
* [DataFrame(doc)](https://spark.apache.org/docs/2.1.0/sql-programming-guide.html)

[sparkDownload]: https://github.com/Shayokh144/Spark_with_Python/blob/master/sparkDownload.png
[jupyterNotebook]: https://github.com/Shayokh144/Spark_with_Python/blob/master/jupyterNoteBook.png
[SparkEcosystem]: https://github.com/Shayokh144/Spark_with_Python-Big_data_Fastest-Smallest_solution-/blob/master/sparkEco.png
