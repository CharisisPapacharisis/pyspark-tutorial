# Pyspark Tutorial

## ℹ️ Overview
This project aims to be a tutorial for pyspark, which is the Python API for Apache Spark. Apache Spark an open-source, distributed computing system designed for large-scale data processing. It enables Python developers to leverage the power of Spark for big data analytics. 

PySpark provides a variety of functions and operations to work efficiently with distributed data. These functions can be broadly divided into two categories: transformations and actions. 

- **Transformations** are lazy operations that define a new RDD (Resilient Distributed Dataset) or DataFrame from an existing one. Examples of transformations, are: filter(), map(), distinct(), groupBy(), join(). "Lazy" means that they are not executed on the spot, but instead they start by creating a logical execution plan.

There is also the differentiation between "narrow" and "wide" transformations, depending on how data is shuffled and partitioned across the cluster.

> `Narrow` transformations are those where each input partition is transformed into one or more output partitions without requiring data shuffling across the network. This means that the data transformation can happen independently within each partition.

> `Wide` transformations require data from multiple partitions to be reshuffled across the network, meaning they often involve an expensive data shuffle. This happens because data needs to be rearranged or aggregated based on keys or partitions from different nodes.

- **Actions** trigger the execution of transformations. They return results to the driver or write output to external storage. Examples of actions, are: show(), count(), first().


## 📝 Repo structure

The repo is organized in two subfolders, "data", and "source". 
- **Data** includes three csv files which I use for showcasing different pyspark operations.
- **Source** includes the full code, in a notebook (.ipynb) format. 

The project shows briefly the practical usage of several pyspark functions.
For example, reading the dataset into a pyspark dataframe, exploring/manipulating it, writing the dataframe in the storage, transforming the pyspark dataframe to pandas, pivoting, using User-Defined-Functions (UDFs), making use of a window function.


## 🚀 Getting Started
Start by cloning the repo. 

To run pyspark **locally in Windows**, you need to install and configure the necessary dependencies. Install Java (JDK 11 or newer should be fine), Apache Spark, a helper tool called winutils.exe (it supports with the Hadoop filesystem on Windows, which Spark uses). You will also need Python, Pyspark, and Jupyter Notebook installed.
Lastly, you will need to set the relevant environmental variables in your PC (e.g.SPARK_HOME, HADOOP_HOME).

Alternatively, You can run PySpark **online** without setting up a local environment by using cloud-based or hosted notebook services. E.g. Google Colab, Databricks Community Edition.