<properties
    pageTitle="I need to increase the number of Network Security rules in my NSG"
    description="How to increase the number of Network Security rules in NSG"
    service="microsoft.network"
    resource="networksecuritygroups"
    authors="radwiv"
    ms.author="radwiv"
    displayOrder="12"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="fde8c5f7-2c71-4082-b81b-faab13b2cf77"
	ownershipId="CloudNet_VirtualNetwork"
/>

# I need to increase the number of Network Security rules in my NSG.

## **Recommended Steps**

Default limit on the number of NSG rules is 200. This can be raised to 400 (Classic) or 500 (Azure Resource Manager) via a support ticket. If you need to increase the number of security rules in your NSG, follow these steps: 

1. Create a [New Support Request](data-blade:Microsoft_Azure_Support.NewSupportRequestBlade)
2. Select the Issue type as "Quota"
3. Select the Quota type as "Networking: Classic" (or Networking: ARM), and enter details of the NSG in details field

## **Recommended Documents**

* [Networking limits](https://docs.azure.cn/azure-subscription-service-limits#networking-limits)
* [Troubleshoot deployment issues for creating a new Virtual machine in Azure](https://docs.azure.cn/virtual-machines/windows/classic/troubleshoot-deployment-new-vm#error-string-lookup)
