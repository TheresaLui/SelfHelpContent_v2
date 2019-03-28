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

see-

https://docs.microsoft.com/en-us/azure/virtual-machines/troubleshooting/troubleshoot-rdp-connection 

https://docs.microsoft.com/en-us/azure/virtual-machines/troubleshooting/detailed-troubleshoot-ssh-connection


## **Recommended Steps**

* Review load balancer service differences on [Azure Stack Networking considerations](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-network-differences)
* Create a Basic load balancer using supported options, including [Azure Portal](https://docs.microsoft.com/azure/load-balancer/quickstart-create-basic-load-balancer-portal), [Azure CLI](https://docs.microsoft.com/azure/load-balancer/quickstart-create-basic-load-balancer-cli), or [an ARM template](https://docs.microsoft.com/azure/load-balancer/load-balancer-get-started-internet-arm-template)
* [Configure port forwarding in Load Balancer](https://docs.microsoft.com/azure/load-balancer/tutorial-load-balancer-port-forwarding-portal)
* [View the public IP addresses that were created by tenant subscriptions](https://docs.microsoft.com/azure/azure-stack/azure-stack-viewing-public-ip-address-consumption#view-the-public-ip-addresses-that-were-created-by-tenant-subscriptions)

## **Recommended Documents**

* [Azure Stack Networking Considerations](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-network-differences)
* Tutorial: [Load balance internet traffic to VMs](https://docs.microsoft.com/azure/load-balancer/tutorial-load-balancer-standard-manage-portal)
* Tutorial: [Load balance internal traffic to VMs](https://docs.microsoft.com/azure/load-balancer/tutorial-load-balancer-basic-internal-portal)
