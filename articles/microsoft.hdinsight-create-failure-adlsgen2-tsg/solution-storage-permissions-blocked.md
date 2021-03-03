<properties
	pageTitle="StoragePermissionsBlockedForMsi"
	description="StoragePermissionsBlockedForMsi"
    service="Microsoft.HDInsight"
    resource="Microsoft.HDInsight/clusters"
	authors="Jacky-hdi"
	ms.author="linjzhu"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="5ba3f3f2-b81c-4657-aace-432d5bb512b1"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# StoragePermissionsBlockedForMsi

<!--issueDescription-->

We have checked the cluster failure and it seems that 'Storage Blob Data Owner' role is not assigned to the Managed Identity ***{MI}*** for the storage account

<!--/issueDescription-->


Please follow the recommended documents to check ADLS Gen2 permission to resolve the issue



## **Recommended Documents**

* [permission issues](https://docs.microsoft.com/en-us/azure/hdinsight/hadoop/hdinsight-troubleshoot-cluster-creation-fails#permissions-issues)
* [hdinsight use ADLS Gen2](https://docs.microsoft.com/en-us/azure/hdinsight/hdinsight-hadoop-use-data-lake-storage-gen2)

