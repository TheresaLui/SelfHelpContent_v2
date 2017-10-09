<properties
    pageTitle="Cluster Creation Fails Due To an Issue With Custom DNS Setup"
    description="Cluster Creation Fails Due To an Issue With Custom DNS Setup"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="ansi12"
    displayOrder="4"
    selfHelpType="resource"
    supportTopicIds="32588505"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, MoonCake"
/>

# Cluster Creation Fails Due To an Issue With Custom DNS Setup
## Error code: InvalidNetworkConfigurationErrorCode
## ErrorDescription
* Virtual Network configuration is not compatible with HDInsight Requirement. Error: 'Failed to connect to Azure Storage Account; Failed to connect to Azure SQL; HostName Resolution failed', Please follow https://go.microsoft.com/fwlink/?linkid=853974 to fix it.

## **Recommended Steps**
The most likely cause for this failure is that Azure's recursive resolvers may be missing in your DNS chain. To fix this issue, please follow the steps in the [troubleshooting guide](https://hdinsight.github.io/ClusterCRUD/hdinsight-customdns.html).

