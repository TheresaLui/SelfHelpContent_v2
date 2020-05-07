<properties
    pageTitle="Azure HDInsights: Spark Unexpected Result"
    description="Azure HDInsights: Spark Unexpected Result"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="genlin"
	ms.author="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32636498"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public,MoonCake, Fairfax, usnat, ussec"
	articleId="5439eff7-79f0-4817-ae46-f580367db1db"
	ownershipId="AzureData_HDInsight"
/>

# Spark Unexpected Results

## **Recommended Steps**

* [IllegalArgumentException](https://docs.microsoft.com/azure/hdinsight/spark/apache-spark-troubleshoot-illegalargumentexception)
* [LISTSTATUS failed with error 0x83090aa2 (Forbidden. ACL verification failed. Either the resource does not exist or the user is not authorized to perform the requested operation.)](https://hdinsight.github.io/ClusterManagement/hdinsight-adlsaccessissues.html)
* [InvalidClassException](https://docs.microsoft.com/azure/hdinsight/spark/apache-spark-troubleshoot-job-fails-invalidclassexception)
* [NativeAzureFileSystem ... RequestBodyTooLarge](https://docs.microsoft.com/azure/hdinsight/spark/apache-spark-troubleshoot-event-log-requestbodytoolarge)
* [Spark Application Fails with OutOfMemoryError](https://docs.microsoft.com/azure/hdinsight/spark/apache-spark-troubleshoot-outofmemory)
* Spark Application Fails with OutOfMemoryError on one node only: This could be due to skew. A frequent solution to skew is to use broadcast plans by changing the broadcast threshold value. The threshold can be configured using `spark.sql.autoBroadcastJoinThreshold`

* To solve issues with YARN applications, the following logs and settings might be helpful:

	* **YARN Timeline Server**: The YARN Timeline server provides generic information on completed applications and framework-specific application information
	* **YARN Application logs**: The application logs can be useful in debugging issues, with aggregated logs being stored in the path `/app-logs/<user>/logs/<applicationId>`
	* **YARN CLI tools**: After connecting to HDInsight cluster using SSH, the YARN logs can be collected using `yarn logs -applicationId <applicationId> -appOwner <user-who-started-the-application>`
	* **YARN ResourceManager UI**: Add `/yarnui/hn/logs/` to the end of the cluster URL to view the YARN logs 

## **Recommended Documents**

* [Access YARN application logs on Linux-based HDInsight](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-access-yarn-app-logs-linux)<br>
* [How do I download Yarn logs from HDInsight cluster?](https://hdinsight.github.io/yarn/yarn-download-logs.html)<br>






