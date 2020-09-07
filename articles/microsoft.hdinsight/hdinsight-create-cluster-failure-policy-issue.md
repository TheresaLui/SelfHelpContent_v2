<properties
    pageTitle="Create failure due to Azure Policy"
    description="Create failure due to Azure Policy"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="genlin"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="Generic"
    supportTopicIds="32681542"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="0a3f2d71-4401-4cf0-8591-a95d9b0ce136"
	ownershipId="AzureData_HDInsight"
/>

# Create failure due to Azure Policy

## **Recommended Steps**

**Azure policies prevent the creation of public IP Address and Load balancers for the HDInsight cluster**

You may receive the following error message:

*Deployments failed due to policy violation: 'Resource 'publicIpgateway-XXXXXXXXXXXXXXXXXXXXXXXX' was disallowed by policy. Policy identifiers: '[{"policyAssignment":{"name":"Deny_Policy_Initiative","id":"/providers/Microsoft.Management/managementGroups/XXXXXXX-XXXX-XXX-XXXX-XXXXXXXXXX/providers/Microsoft.Authorization/policyAssignments/9f2dc84d5f7f4e7299f655fe"},**"policyDefinition":{"name":" Deny_PublicIP_policy_Rule","id":"/providers/Microsoft.Management/managementGroups/ XXXXXXX-XXXX-XXX-XXXX-XXXXXXXXXX /providers/Microsoft.Authorization/policyDefinitions/ XXXXXXX-XXXX-XXX-XXXX-XXXXX**"*

To resolve this issue, follow these steps:

1. Go to the Azure Portal and search for Policy
2. On the Policy page, go to **Assignments** and remove the policy identified in the error message to allow public IP creation
1. Try to recreate HDInsight cluster. The policy can be populated after the cluster is created.

For more information azure Azure policy, see [Tutorial: Create and manage policies to enforce compliance](https://docs.microsoft.com/azure/governance/policy/tutorials/create-and-manage).

**Traffics are denied by a firewall rule on virtual network or Storage Accounts**

To resolve this issue, follow these steps:

- Check the firewall rules and  make sure that they are not blocking traffics between your Storage account and the HDInsight virtual network. For more information, see [Configure Azure Storage firewalls and virtual networks](https://docs.microsoft.com/azure/storage/common/storage-network-security).
- Always allow traffic from the IP addresses of Azure Health and management services:

    - 168.61.49.99
    - 23.99.5.239
    - 168.61.48.131
    - 138.91.141.162

- These IP addresses Destination must be set at *:433 and a Direction of "Inbound"
- If your cluster is in a specific region, add the respective source IP. For the list of the IP addresses, see [Health and management services: Specific regions](https://docs.microsoft.com/azure/hdinsight/hdinsight-management-ip-addresses#health-and-management-services-specific-regions).
- If you are using either Express Route or your own custom DNS server, see [Connecting multiple networks](https://docs.microsoft.com/azure/hdinsight/hdinsight-plan-virtual-network-deployment#multinet)

## **Recommended Documents**

* [Create Cluster Error Dictionary](https://docs.microsoft.com/azure/hdinsight/create-cluster-error-dictionary)
