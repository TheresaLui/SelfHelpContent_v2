<properties
    pageTitle="Spark application failed with OutOfMemoryError"
    description="Spark application failed with OutOfMemoryError"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="bharathsreenivas"
    displayOrder="4"
    selfHelpType="resource"
    supportTopicIds="32511213"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, MoonCake"
/>

# Spark application failed with OutOfMemoryError

The most likely cause of this exception is not enough heap memory allocated to the Java Virtual Machine (JVM) that are launched as executors or driver as part of the Spark application.

## **Recommended Steps**
1. Determine the maximum size of the data the Spark application will handle. A guess can be made based on the maximum of the size of input data, the intermediate data produced by transforming the input data and the output data produced further transforming the intermediate data. This can be an iterative process also if formal initial guess is not possible.
2. Make sure that the HDInsight cluster to be used has enough resources in terms of memory and also cores to accommodate the Spark application. This can be determined by viewing the Cluster Metrics section of the YARN UI of the cluster for the values of Memory Used vs. Memory Total and VCores Used vs. VCores Total.
3. Set the Spark configurations to appropriate values that do not exceed 90% of the available memory and cores as viewed by YARN yet well within the memory requirement of the Spark application.

## **Recommended documents**
[Spark Application Failed with OutOfMemoryError](https://hdinsight.github.io/spark/spark-application-failure-with-outofmemoryerror.html)<br>
