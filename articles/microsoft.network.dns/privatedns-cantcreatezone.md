<properties 
    pageTitle="I can't create a new private DNS zone"
    description="I am unable to create a new private DNS zone in the Azure DNS service."
    service="microsoft.network"
    resource="privateDnsZones"
    authors="rohinkoul"
    ms.author="rohink"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public,fairfax,mooncake,blackforest, usnat, ussec"
	articleId="privatedns-cantcreatezone"
	ownershipId="CloudNet_DNS"
/>

# I can't create a new private DNS zone

## **Recommended Steps**

To resolve common issues, try one or more of the following steps:

* Review [Audit logs](data-blade:Microsoft_Azure_Insights.AzureDiagnosticsBladeWithParameter) to determine the failure reason
* Each private DNS zone name must be unique within its resource group. That is, two private DNS zones with the same name cannot share a resource group. Try using a different zone name, or a different resource group.
* You may see an error "You have reached or exceeded the maximum number of zones in subscription {subscription id}." Either use a different Azure subscription, delete some zones, or contact Azure Support to raise your subscription limit.
* You may not have appropriate [RBAC](https://docs.microsoft.com/azure/role-based-access-control/overview) permissions to create the private DNS zone. Please make sure you have "Private DNS Zone Contributor" Role assigned.
* Are you trying to create single label zones? Azure DNS private zones do not support creation of single label domains. Please ensure that your private DNS zone name has at least two labels separated by a dot (.).

## **Recommended Documents**

* [Create private DNS zones](https://docs.microsoft.com/azure/dns/private-dns-portal)
