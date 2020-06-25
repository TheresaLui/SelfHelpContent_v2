<properties
    pageTitle="Configure, Set up, or Manage multiple Public IPs"
    description="Configure, Set up, or Manage multiple Public IPs"
    service="microsoft.network"
    resource="azurefirewalls"
    authors="genlin"
    ms.author="mariliu"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32675670"
    resourceTags=""
    productPesIds="16556"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="c0c91d65-1022-45d9-9b34-f9cf8fdca419"
	ownershipId="CloudNet_AzureFirewall"
/>
# Configure, set up, or manage multiple Public IPs

## **Recommended Documents**

- [Multiple public IPs](https://docs.microsoft.com/azure/firewall/overview#multiple-public-ips-public-preview)
- [Deploy an Azure Firewall with multiple public IP addresses using Azure PowerShell](https://docs.microsoft.com/azure/firewall/deploy-multi-public-ip-powershell)

NOTE: During the public preview, if you add or remove a public IP address from a running firewall, the existing inbound connectivity using Destination Network Address Translation (DNAT) rules may not function for 40 ~ 120 seconds. There is no impact to outbound connectivity. This problem will be fixed by the General Availability release.


