<properties
    pageTitle="Azure Stack Load Balancers"
    description="Azure Stack Load Balancers for User Environment"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629223"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax"
    articleId="b98cb657-d25f-4445-a5a4-bfb14de1e04e"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Load Balancer for User Environment

Azure Stack networking has many of the features provided by Azure networking, including Azure Networking Load Balancer resources. Load balancing provides a higher level of availability and scale by spreading incoming requests across multiple virtual machines.

## **Recommended Steps**

* Review load balancer service differences on [Azure Stack Networking considerations](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-network-differences)
* Create a Basic load balancer using supported options, including [Azure Portal](https://docs.microsoft.com/azure/load-balancer/quickstart-create-basic-load-balancer-portal), [Azure CLI](https://docs.microsoft.com/azure/load-balancer/quickstart-create-basic-load-balancer-cli), or [an ARM template](https://docs.microsoft.com/azure/load-balancer/load-balancer-get-started-internet-arm-template)
* [Configure port forwarding in Load Balancer](https://docs.microsoft.com/azure/load-balancer/tutorial-load-balancer-port-forwarding-portal)
* [View the public IP addresses that were created by tenant subscriptions](https://docs.microsoft.com/azure/azure-stack/azure-stack-viewing-public-ip-address-consumption#view-the-public-ip-addresses-that-were-created-by-tenant-subscriptions)

## **Recommended Documents**

* [Azure Stack Networking Considerations](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-network-differences)
* [What is Azure Load Balancer?](https://docs.microsoft.com/azure/load-balancer/load-balancer-overview)
* Tutorial: [Load balance internet traffic to VMs](https://docs.microsoft.com/azure/load-balancer/tutorial-load-balancer-standard-manage-portal)
* Tutorial: [Load balance internal traffic to VMs](https://docs.microsoft.com/azure/load-balancer/tutorial-load-balancer-basic-internal-portal)
