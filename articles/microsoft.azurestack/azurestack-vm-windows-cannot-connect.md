<properties
    pageTitle="Azure Stack Windows VM connectivity issues"
    description="Azure Stack Windows VM connectivity issues"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="genlin"
    ms.author="mquian"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32663890"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="6f641910-1007-4135-b8d1-85ab25fa1503"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Windows VM connectivity issues

Connectivity to an Azure Stack VM can be affected by networking issues in the Azure Stack environment, on the customer datacenter network, or due to an issue with the VM itself. The following topics cover common support questions. 

4 out of 5 customers resolved their issue using the guides listed below.<br>

## **Recommended Steps**

* Confirm the expected ports are allowed by the [Network Security Group (NSG)](https://docs.microsoft.com/azure/virtual-network/manage-network-security-group#view-all-security-rules) or [configure port forwarding in Load Balancer](https://docs.microsoft.com/azure/load-balancer/tutorial-load-balancer-port-forwarding-portal#create-an-inbound-nat-port-forwarding-rule)
* For RDP connection issues for Windows VMs on Azure Stack:

  * [Basic troubleshooting](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-connection)
  * [Advanced troubleshooting](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/detailed-troubleshoot-rdp)

## **Recommended Documents**

- [Troubleshoot specific RDP errors](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-connection#troubleshoot-specific-rdp-errors)