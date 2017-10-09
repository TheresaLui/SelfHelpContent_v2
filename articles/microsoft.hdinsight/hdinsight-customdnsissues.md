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

# Cluster Creation Fails Due To an Issue With Custom DNS Setup (Error code: InvalidNetworkConfigurationErrorCode)
* ErrorDescription: Virtual Network configuration is not compatible with HDInsight Requirement. Error: 'Failed to connect to Azure Storage Account; Failed to connect to Azure SQL; HostName Resolution failed', Please follow https://go.microsoft.com/fwlink/?linkid=853974 to fix it.

## **Recommended Steps**
The most likely cause for this failure is that Azure's recursive resolvers may be missing in your DNS chain. DNS servers within a virtual network can forward DNS queries to Azure's recursive resolvers to resolve hostnames within that virtual network. Access to Azure's recursive resolvers is provided via the virtual IP 168.63.129.16. To resolve the issue, this IP needs to be added yo your DNS chain. See the [troubleshooting guide](https://hdinsight.github.io/ClusterCRUD/hdinsight-customdns) for details.

## **Recommended documents**
[Cluster Creation Fails Due To an Issue With Custom DNS Setup](https://hdinsight.github.io/ClusterCRUD/hdinsight-udr)<br>
