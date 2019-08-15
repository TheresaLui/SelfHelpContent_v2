<properties
    pageTitle="Cluster Creation Fails Due To an Issue With User-Defined Rules"
    description="Cluster Creation Fails Due To an Issue With User-Defined Rules"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="ansi12"
    ms.author="ansiva"
    displayOrder="37"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="hdinsight-udrissue-mooncake"
/>

# Cluster Creation Fails Due To an Issue With User-Defined Rules
## Error codes: InvalidNetworkConfigurationErrorCode
## Errors Description:

* Virtual Network configuration is not compatible with HDInsight Requirement. Error: 'Failed to connect to Azure Storage Account' or  'Failed to connect to Azure SQL'

## **Recommended Steps**

Please follow the steps listed in the [troubleshooting guide](https://hdinsight.github.io/ClusterCRUD/hdinsight-vnet#2-errordescription-contains-failed-to-connect-to-azure-storage-account-or-failed-to-connect-to-azure-sql) to make sure that your User-Defined Rules are set up correctly.
