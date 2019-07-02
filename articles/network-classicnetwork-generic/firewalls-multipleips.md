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
    cloudEnvironments="public"
    articleId="c0c91d65-1022-45d9-9b34-f9cf8fdca419"
/>
# Configure, set up, or manage multiple Public IPs

## **Recommended Documents**

- [Availability Zones (public preview)](https://docs.microsoft.com/azure/firewall/overview#availability-zones-public-preview)
- [Deploy an Azure Firewall with Availability Zones using Azure PowerShell](https://docs.microsoft.com/azure/firewall/deploy-availability-zone-powershell)

NOTE: During the public preview, if you add or remove a public IP address from a running firewall, the existing inbound connectivity using Destination Network Address Translation (DNAT) rules may not function for 40 ~ 120 seconds. There is no impact to outbound connectivity. This problem will be fixed by the General Availability release.
