<properties 

    pageTitle="I can't create a new DNS zone"

    description="I am unable to create a new DNS zone in the Azure DNS service."

    service="microsoft.network"

    resource="dnszones"

    authors="jtuliani"

    displayOrder="1"

    selfHelpType="generic"

    supportTopicIds=""

    productPesIds=""

    resourceTags=""​

    cloudEnvironments="public"  

 />

# I can't create a new DNS zone

## Recommended steps

To resolve common issues, try one or more of the following:

1.	Review [Audit logs](data-blade:Microsoft_Azure_Insights.AzureDiagnosticsBladeWithParameter) to determine the failure reason.
2.	Each DNS zone name must be unique within its resource group. That is, two DNS zones with the same name cannot share a resource group. Try using a different zone name, or a different resource group.
3.	If you see an error "You have reached or exceeded the maximum number of zones in subscription {subscription id}", then either use a different Azure subscription, delete some zones, or contact Azure Support to raise your subscription limit, then try again.
4.	If you see an error "The zone '{zone name}' is not available", this means Azure DNS was unable to allocate name servers for this DNS zone. Try using a different zone name. Alternatively, if you are the domain name owner, contact Azure Support, who can allocate name servers for you.

If the above steps don't resolve the issue, please open an Azure Support ticket.


## Recommended documents

[DNS zones and records](https://docs.microsoft.com/azure/dns/dns-zones-records)
<br>
[Create a DNS zone](https://docs.microsoft.com/azure/dns/dns-getstarted-create-dnszone-portal)
