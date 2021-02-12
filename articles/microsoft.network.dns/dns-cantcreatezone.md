<properties 
    pageTitle="I can't create a new DNS zone"
    description="I am unable to create a new DNS zone in the Azure DNS service."
    service="microsoft.network"
    resource="dnszones"
    authors="jtuliani"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="1386f342-42ab-49b9-8296-d6a4f30209bf"
	ownershipId="CloudNet_DNS"
/>

# I can't create a new DNS zone

## **Recommended steps**

To resolve common issues, try one or more of the following steps:

1.	Review [Audit logs](data-blade:Microsoft_Azure_Insights.AzureDiagnosticsBladeWithParameter) to determine the failure reason.
2.	Each DNS zone name must be unique within its resource group. That is, two DNS zones with the same name cannot share a resource group. Try using a different zone name, or a different resource group.
3.	You may see an error "You have reached or exceeded the maximum number of zones in subscription {subscription id}." Either use a different Azure subscription, delete some zones, or contact Azure Support to raise your subscription limit.
4.	You may see an error "The zone '{zone name}' is not available." This error means that Azure DNS was unable to allocate name servers for this DNS zone. Try using a different zone name. Alternatively, if you are the domain name owner, contact Azure support, who can allocate name servers for you.

If the above steps don't resolve the issue, please post this issue to our [community support forum on MSDN](https://social.msdn.microsoft.com/Forums/en-US/home?forum=WAVirtualMachinesVirtualNetwork) or open an Azure support request.

## **Recommended documents**

[DNS zones and records](https://docs.microsoft.com/azure/dns/dns-zones-records)
<br>
[Create a DNS zone](https://docs.microsoft.com/azure/dns/dns-getstarted-create-dnszone-portal)
