<properties
    pageTitle="Cluster Creation Fails Due To an Issue With Custom DNS Setup"
    description="Cluster Creation Fails Due To an Issue With Custom DNS Setup"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="ansi12"
    displayOrder="17"
    selfHelpType="resource"
    supportTopicIds="32588505"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, MoonCake"
/>

# Cluster Creation Fails With InvalidNetworkConfigurationErrorCode
## ErrorDescription
Virtual Network configuration is not compatible with HDInsight Requirement. Error: 'HostName Resolution failed'

## **Recommended Steps**
The most likely cause for this failure is that Azure's recursive resolvers may be missing in your DNS chain. To fix this issue, please follow the steps in the [troubleshooting guide](https://hdinsight.github.io/ClusterCRUD/hdinsight-vnet#1-errordescription-contains-hostname-resolution-failed).

