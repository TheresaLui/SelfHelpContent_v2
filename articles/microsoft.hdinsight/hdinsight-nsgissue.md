<properties
    pageTitle="Cluster Creation Fails Due To an Issue With Custom DNS Setup"
    description="Cluster Creation Fails Due To an Issue With Custom DNS Setup"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="ansi12"
    displayOrder="4"
    selfHelpType="resource"
    supportTopicIds="32588506"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, MoonCake"
/>

# Cluster Creation Fails Due To an Issue With Custom DNS Setup
## Error codes: InvalidNetworkSecurityGroupSecurityRules or InvalidNetworkConfigurationErrorCode
## You might see one of the following errors descriptions:
* The security rules in the Network Security Group configured with subnet does not allow required inbound and/or outbound connectivity. For more information please visit http://go.microsoft.com/fwlink/?linkid=785236 or contact support.
* Virtual Network configuration is not compatible with HDInsight Requirement. Error: 'Failed to connect to Azure Storage Account; Failed to connect to Azure SQL; HostName Resolution failed', Please follow https://go.microsoft.com/fwlink/?linkid=853974 to fix it.

## **Recommended Steps**
There is probably a problem with the inbound or outbound network security rules. Please follow the steps listed in the [troubleshooting guide](https://hdinsight.github.io/ClusterCRUD/hdinsight-nsg) to resolve the issue.
