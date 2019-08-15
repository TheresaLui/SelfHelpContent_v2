<properties
    pageTitle="Cluster Creation Fails Due To an Issue With Network Security Group"
    description="Cluster Creation Fails Due To an Issue With Network Security Group"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="ansi12"
    ms.author="ansiva"
    displayOrder="28"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="hdinsight-nsgissue-mooncake"
/>

# Cluster Creation Fails With InvalidNetworkSecurityGroupSecurityRules or InvalidNetworkConfigurationErrorCode
## Errors Descriptions

* The security rules in the Network Security Group configured with subnet does not allow required inbound and/or outbound connectivity.
* Virtual Network configuration is not compatible with HDInsight Requirement. Error: 'Failed to connect to Azure Storage Account' or 'Failed to connect to Azure SQL'

## **Recommended Steps**

* For **InvalidNetworkSecurityGroupSecurityRules**, please follow this [troubleshooting guide](https://hdinsight.github.io/ClusterCRUD/hdinsight-nsg).
* For **InvalidNetworkConfigurationErrorCode**, please follow this [troubleshooting guide](https://hdinsight.github.io/ClusterCRUD/hdinsight-vnet#2-errordescription-contains-failed-to-connect-to-azure-storage-account-or-failed-to-connect-to-azure-sql).
