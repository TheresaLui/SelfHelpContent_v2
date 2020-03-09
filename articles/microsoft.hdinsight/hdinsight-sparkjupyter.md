<properties
    pageTitle="Jupyter notebooks on HDInsight spark clusters"
    description="Create jupyter notebooks to execute Spark Jobs"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="csunilkumar"
    ms.author="sunilkc"
    displayOrder="30"
    selfHelpType="resource"
    supportTopicIds="32636484"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, Fairfax"
    articleId="hdinsight-sparkjupyter"
	ownershipId="AzureData_HDInsight"
/>

# Azure HDInsight: Working with Jupyter notebook on Apache Spark clusters in Azure HDInsight

As of January 29, 2020, there is an active issue in which you may receive an error when attempting to use a Jupyter notebook. Use the steps below to fix the issue. You can also refer to this [MSDN post](https://social.msdn.microsoft.com/Forums/en-us/8c763fb4-79a9-496f-a75c-44a125e934ac/hdinshight-create-not-create-jupyter-notebook?forum=hdinsight) or this [StackOverflow post](https://stackoverflow.com/questions/59687614/azure-hdinsight-jupyter-notebook-not-working/59831103) for up to date information, or to ask additional questions.

**Errors**

* ValueError: Cannot convert notebook to v5 because that version doesn't exist
* Error loading notebook An unknown error occurred while loading this notebook. This version can load notebook formats v4 or earlier.

**Cause** 

The _version.py file on the cluster was updated to 5.x.x instead of 4.4.x.## or Ambari needs to be restarted.

**Solution**

If you create a new Jupyter notebook and receive one of the errors listed above, do the following:

1. Open Ambari in a web browser by going to https://CLUSTERNAME.azurehdinsight.net, where CLUSTERNAME is the name of your cluster
1. In Ambari, on the left menu, click **Jupyter**, then on **Service Actions**, click **Stop**
1. ssh into the cluster headnode where the Jupyter service is running
1. Open the file /usr/bin/anaconda/lib/python2.7/site-packages/nbformat/_version.py in sudo mode
1. Check the value of version_info
1. If the value of version_info is set to: 

   version_info = (5, 0, 3)
   
   Then modify the entry to: 

   version_info = (4, 4, 0)
   
   And save the file

   If version_info is already set to (4, 4, 0), then continue to the next step as only Ambari needs to be restarted, no additional changes are needed.

1. Go back to Ambari, and in **Service Actions**, click **Restart All**

## **Recommended Documents**

**Jupyter notebooks**

* [Create and configure Jupyter notebooks](https://docs.microsoft.com/azure/hdinsight/spark/apache-spark-jupyter-notebook-kernels)
* [Use external packages with Jupyter notebooks](https://docs.microsoft.com/azure/hdinsight/spark/apache-spark-jupyter-notebook-use-external-packages)

**Zeppelin notebooks**

* [Use Apache Zeppelin notebooks with Apache Spark cluster on Azure HDInsight](https://docs.microsoft.com/azure/hdinsight/spark/apache-spark-zeppelin-notebook)
