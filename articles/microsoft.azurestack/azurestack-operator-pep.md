<properties
  pagetitle="Using the Azure Stack Privileged Endpoint (PEP)"
  service="microsoft.azurestack"
  resource="registrations"
  ms.author="v-myoung"
  selfhelptype="Generic"
  supporttopicids="32629247"
  resourcetags=""
  productpesids="16226"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azurestack-operator-pep"
  ownershipid="StorageMediaEdge_AzureStack_Hub" />
# Using the Azure Stack Privileged Endpoint (PEP)

As an Azure Stack operator, you should use the administrator portal, PowerShell, or Azure Resource Manager APIs for most day-to-day management tasks. However, for some less common operations, you need to use the privileged endpoint (PEP).

Users who need support with using the PEP often just need to know their IP address. To find your IP address, sign in to the Administrator portal and select **Region Management** > **Properties**. Once you know the IP address, you can follow the recommended steps to use the PEP.

If you're using a Hardware Lifecycle Host running version 2005 or later, you can instead use the [Operator Access Workstation](https://docs.microsoft.com/azure-stack/operator/operator-access-workstation) (OAW) to use the PEP.

## **Recommended Steps**

1. [Access the Privileged Endpoint (PEP)](https://docs.microsoft.com/azure/azure-stack/azure-stack-privileged-endpoint#access-the-privileged-endpoint) and [follow best practices](https://docs.microsoft.com/azure/azure-stack/azure-stack-privileged-endpoint#tips-for-using-the-privileged-endpoint) to perform low-level tasks, such as [collecting diagnostic logs](https://docs.microsoft.com/azure/azure-stack/azure-stack-diagnostics#log-collection-tool).
2. To create the transcript logs, [close the privileged endpoint session](https://docs.microsoft.com/azure/azure-stack/azure-stack-privileged-endpoint#close-the-privileged-endpoint-session) when you are done using it

## **Recommended Documents**

- [Using the privileged endpoint in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-privileged-endpoint)
- [Azure Stack Log Collection Tool](https://docs.microsoft.com/azure/azure-stack/azure-stack-diagnostics#log-collection-tool)
