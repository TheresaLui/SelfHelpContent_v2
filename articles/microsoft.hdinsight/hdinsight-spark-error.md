<properties
    pageTitle="Spark application failed with OutOfMemoryError"
    description="Spark application failed with OutOfMemoryError"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="bharathsreenivas"
	ms.author="v-anukar"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629134"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, MoonCake, Fairfax, usnat, ussec"
	articleId="94707938-9b6f-4d8a-a78a-de57c2879a5c"
	ownershipId="AzureData_HDInsight"
/>

# Spark Application Failed with OutOfMemoryError

The most likely cause of this exception is not enough heap memory allocated to the Java Virtual Machine (JVM) that is/are launched as executors or drivers as part of the Spark application.

## **Recommended Steps**

* Determine the maximum size of the data the Spark application will handle. A guess can be made based on the maximum of the size of input data, the intermediate data produced by transforming the input data, and the output data produced further transforming the intermediate data. This can also be an iterative process, if an initial guess is not possible.

* Make sure that the HDInsight cluster to be used has enough resources (memory and cores) to accommodate the Spark application. This can be determined by viewing the Cluster Metrics section of the YARN UI of the cluster for the values of Memory Used vs. Memory Total, and VCores Used vs. VCores Total.

* Set the Spark configurations to appropriate values that do not exceed 90% of the available memory and cores as viewed by YARN, yet well within the memory requirement of the Spark application.

## **Recommended Documents**

* [Spark Application Failed with OutOfMemoryError](https://hdinsight.github.io/spark/spark-application-failure-with-outofmemoryerror.html)<br>
