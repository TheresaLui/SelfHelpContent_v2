<properties
    pageTitle="Azure Stack Connectivity to Virtual Machines"
    description="Resolve issues with connectivity to Azure Stack VMs"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629202"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
    articleId="azurestack-network-connectivity"
/>

# Resolve issues with connectivity to Azure Stack VMs

Connectivity to Azure Stack VMs can be affected by networking issues in the Azure Stack environment, on the customer datacenter network, or due to an issue with the VM itself.

## **Recommended Steps**

* Confirm the expected ports are allowed by the [Network Security Group (NSG)](https://docs.microsoft.com/azure/virtual-network/manage-network-security-group#work-with-security-rules) or [configure port forwarding in Load Balancer](https://docs.microsoft.com/azure/load-balancer/tutorial-load-balancer-port-forwarding-portal)
* For RDP connection issues for Windows VMs on Azure Stack:

  * Basic: [Troubleshoot Remote Desktop connections to an Azure virtual machine](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-connection#troubleshoot-using-the-azure-portal)
  * Advanced: [Detailed troubleshooting steps for remote desktop connection issues to Windows VMs in Azure](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/detailed-troubleshoot-rdp)

* For SSH connection issues for Linux VMs on Azure Stack:

  * Basic: [Troubleshoot SSH connections to an Azure Linux VM that fails, errors out, or is refused](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-ssh-connection)
  * Advanced: [Detailed SSH troubleshooting steps for issues connecting to a Linux VM in Azure](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/detailed-troubleshoot-ssh-connection)

## **Recommended Documents**

* [Azure Stack Networking Considerations](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-network-differences)
* Tutorial: [Load balance internet traffic to VMs](https://docs.microsoft.com/azure/load-balancer/tutorial-load-balancer-standard-manage-portal)
* Tutorial: [Load balance internal traffic to VMs](https://docs.microsoft.com/azure/load-balancer/tutorial-load-balancer-basic-internal-portal)
