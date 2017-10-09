<properties
    pageTitle="Cluster Creation Fails Due To an Issue With User-Defined Rules"
    description="Cluster Creation Fails Due To an Issue With User-Defined Rules"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="ansi12"
    displayOrder="4"
    selfHelpType="resource"
    supportTopicIds="32588507"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, MoonCake"
/>

# Cluster Creation Fails Due To an Issue With User-Defined Rules
## Error codes: InvalidNetworkConfigurationErrorCode
## Errors Description:
* Virtual Network configuration is not compatible with HDInsight Requirement. Error: 'Failed to connect to Azure Storage Account; Failed to connect to Azure SQL; HostName Resolution failed', Please follow https://go.microsoft.com/fwlink/?linkid=853974 to fix it.

## **Recommended Steps**
If you have set up User-Defined Rules for the cluster, please follow the steps listed in the [troubleshooting guide](https://hdinsight.github.io/ClusterCRUD/hdinsight-udr.html) to make sure that the rules are set up correctly.
