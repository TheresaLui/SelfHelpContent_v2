<properties
    pageTitle="Cluster Creation Fails Due To an Issue With Custom DNS Setup"
    description="Cluster Creation Fails Due To an Issue With Custom DNS Setup"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="ansi12"
    ms.author="jaserano"
    displayOrder="17"
    selfHelpType="resource"
    supportTopicIds="32636488"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, MoonCake"
    articleId="6a60e737-a15c-44df-8320-273b54797713"
/>

# Cluster Creation Fails With InvalidNetworkConfigurationErrorCode

Virtual Network configuration is not compatible with HDInsight Requirement. Error: 'HostName Resolution failed'

## **Recommended Steps**

The most likely cause for this failure is that Azure's recursive resolvers may be missing in your DNS chain. To fix this issue, please follow the steps in the [troubleshooting guide](https://hdinsight.github.io/ClusterCRUD/hdinsight-vnet#1-errordescription-contains-hostname-resolution-failed).
