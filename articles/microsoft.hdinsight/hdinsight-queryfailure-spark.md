<properties
 pageTitle="Azure HDInsights Query Failure - Spark "
 description="Azure HDInsights Query Failure - Spark "
 service="microsoft.hdinsight"
 resource="clusters"
 authors="TobyTu"
 ms.author="deeptivu"
 displayOrder=""
 selfHelpType="generic"
 supportTopicIds="32636496"
 resourceTags=""
 productPesIds="15078"
 cloudEnvironments="public, MoonCake, Fairfax, usnat, ussec"
 articleId="302b8254-83e6-4005-9d2e-891f19ebc0f3"
 ownershipId="AzureData_HDInsight"
/>

# Azure HDInsights Query Failure - Spark

## **Recommended Steps**

1. Check Resource Utilization

   * Verify that the HDInsight cluster to be used has enough memory and cores to accommodate the Spark application. To determine this, view the Cluster Metrics section of the cluster's YARN UI, and locate the values of **Memory Used** vs. **Memory Total** and **VCores Used** vs. **VCores Total**.
   * If you do not have enough resources to accommodate your Spark application/job, scale up the cluster to ensure the cluster has enough memory and cores.

1. Check the supporting JAR files being used to execute the job. Check that additional JAR files libraries are in the right class path, and make use of following class path if any additional jar files need to be loaded:

     * spark.driver.extraClassPath
     * spark.yarn.user.classpath.first
     * spark.executor.extraClassPath

 If the JAR file libraries aren't in the right class path, copy the jars to the required class path.

1. Check Storage (WASB or ADL)

   Verify that permissions to the store are correct, then log into to the cluster and list the JAR file from the Headnode using the following set of CMD instructions:

     ```
     hdfs dfs -ls wasbs://CONTAINERNAME@STORAGEACCOUNT.blob.core.windows.net/sampledata1/
     hdfs dfs -ls wasbs:///sampledata2/
     hdfs dfs -ls /sampledata3/
     ```

   * If the permissions aren't correct, check that the user accessing the storage has Read/Write/Execute (RWX) permissions on that folder.
   * Have the user run the following SSH command "hdfs dfs -ls /" This command will list the permissions for the root folder of the staorage. This will help to determine if they have RWX permissions.

1. Check the Livy logs

   * If your Spark Job(s) use LIVY from Jupyter or ADF, check the Livy logs. A timeout can result when JAR files are too big, when there are too many resources to distribute, or when file copying between storages is taking too long. If Livy doesn't get the application ID from YARN within two minutes, then the LIVY batch will fail.
   * To resolve this, reduce the size or JAR file or increase the timeout value `livy.server.yarn.app-lookup-timeout`.

1. End the job from the Yarn UI

   If your Spark Job is stuck/application hangs, end the job from the Yarn UI, or run Yarn Kill CMD:
   
   * ``yarn application -kill <application_id>``.
   
   If ending the job does not resolve the issue, check whether LIVY has returned an application ID. If no application ID has been returned, follow these steps:

     **Note**: Stuck jobs are listed in the Running state.

     1. Track the application in the Spark UI and look at the Stages Tab
     1. Look at the duration of the various stages and identify which stages seem like anomalies
     1. Take a screenshot of the DAG Visualization and present this information to the support engineer whom you work with

### **Solutions to common errors encountered**

* [IllegalArgumentException](https://hdinsight.github.io/spark/spark-application-fails-IllegalArgumentException.html)
* [LISTSTATUS failed with error 0x83090aa2 (Forbidden. ACL verification failed. Either the resource does not exist or the user isn't authorized to perform the requested operation.)](https://hdinsight.github.io/ClusterManagement/hdinsight-adlsaccessissues.html)
* [InvalidClassException](https://hdinsight.github.io/spark/spark-class-version-mismatch-InvalidClassException.html)
* [NativeAzureFileSystem ... RequestBodyTooLarge](https://hdinsight.github.io/spark/spark-stream-driver-logs-error-requestbodytoolarge.html)
* [Spark Application Fails with OutOfMemoryError](https://hdinsight.github.io/spark/spark-application-failure-with-outofmemoryerror.html)

## **Recommended Documents**

* [Debug Apache Spark jobs running on Azure HDInsight](https://docs.microsoft.com/azure/hdinsight/spark/apache-spark-job-debugging)
