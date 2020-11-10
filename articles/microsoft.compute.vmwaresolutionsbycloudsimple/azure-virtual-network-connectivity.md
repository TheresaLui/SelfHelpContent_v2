<properties
    pageTitle="Access Azure VMware Solution by CloudSimple - Portal" 
    description="Describes how to access VMware Solution by CloudSimple portal from Azure portal"
    infoBubbleText="Problems related to Azure virtual network connection of a subscription from CloudSimple network, VMware VMs. See details on the right."
    ms.service="azure-vmware-cloudsimple"
    authors="dikamath, sharaths-cs" 
    ms.author="dikamath, b-shsury, v-rabmah"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32637608"
    resourceTags=""
    productPesIds="16733"
    cloudEnvironments="public, fairfax, usnat, ussec" 
    articleId="8822e85f-acda-4b67-926c-cc73f52543a5"    
	ownershipId="Compute_VirtualMachines_Content"
/>

# Troubleshooting Azure virtual network connection 

## **Recommended Steps**

* Check that the Virtual Network Gateway that links to your Azure virtual network to CloudSimple is of type **ExpressRoute**
* Check if a gateway subnet created in the virtual network
* Check if ExpressRoute Gateway already connected to another ExpressRoute circuit in the same peering location
* Check that the correct connection type selected
* Check that the virtual network in the same location as the Virtual Network Gateway
* Check if there is a subnet overlap with the private cloud
* Check if the subnet overlaps with another peered virtual network
* Check if you are linking more than 10 virtual networks in a standard ExpressRoute Circuit


## **Recommended Documents**

<span title="Problems related to Azure virtual network connection of a subscription from CloudSimple network, VMware VMs">

* [Azure Virtual Network Connection using ExpressRoute](https://docs.microsoft.com/azure/vmware-cloudsimple/azure-expressroute-connection)<br>
</span>


