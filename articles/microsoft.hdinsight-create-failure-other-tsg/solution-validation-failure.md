<properties
	pageTitle="InvalidDocumentErrorCode"
	description="InvalidDocumentErrorCode"
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
	articleId="0cd594f2-d317-4d7f-a3ec-e0b010ef8cf6"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# InvalidDocumentErrorCode

<!--issueDescription-->

***INTERNAL CONTENT DO NOT PROVIDE TO CUSTOMER***

Check the ***{Validation Failure}*** in ErrorInfoAsJson in IaasClusterCRUDEvent in previous step

<!--/issueDescription-->

Please try to check Pssible RCA to mitigate the issue:


## **Possible RCA**

* [Custom metastore %100 DTU](https://supportability.visualstudio.com/AzureHDinsight/_wiki/wikis/AzureHDinsight/349605/Cluster_creation_failure_from_Metastore_DB_DTU_Overutilization)
* [InvalidTopologyException in spark cluster creation](https://supportability.visualstudio.com/AzureHDinsight/_wiki/wikis/AzureHDinsight/349531/Spark-cluster-creation-failure-due-to-missing-components)
