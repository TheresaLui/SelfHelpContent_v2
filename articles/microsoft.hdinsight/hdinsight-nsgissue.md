<properties
    pageTitle="Cluster Creation Fails Due To an Issue With Network Security Group"
    description="Cluster Creation Fails Due To an Issue With Network Security Group"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="ansi12"
    displayOrder="19"
    selfHelpType="resource"
    supportTopicIds="32588506"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, MoonCake, Fairfax, usnat, ussec"
	articleId="bcafe3cc-2e04-4fc5-a352-e62dd714a044"
	ownershipId="AzureData_HDInsight"
/>

# Cluster Creation Fails With InvalidNetworkSecurityGroupSecurityRules or InvalidNetworkConfigurationErrorCode
## Errors Descriptions
* The security rules in the Network Security Group configured with subnet does not allow required inbound and/or outbound connectivity.
* Virtual Network configuration is not compatible with HDInsight Requirement. Error: 'Failed to connect to Azure Storage Account' or 'Failed to connect to Azure SQL'

## **Recommended Steps**
* For **InvalidNetworkSecurityGroupSecurityRules**, please follow this [troubleshooting guide](https://hdinsight.github.io/ClusterCRUD/hdinsight-nsg).
* For **InvalidNetworkConfigurationErrorCode**, please follow this [troubleshooting guide](https://hdinsight.github.io/ClusterCRUD/hdinsight-vnet#2-errordescription-contains-failed-to-connect-to-azure-storage-account-or-failed-to-connect-to-azure-sql).
