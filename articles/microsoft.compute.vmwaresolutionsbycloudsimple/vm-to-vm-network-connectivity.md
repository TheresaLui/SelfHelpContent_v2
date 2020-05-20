<properties
    pageTitle="Access Azure VMware Solution by CloudSimple - Portal" 
    description="Describes how to access VMware Solution by CloudSimple portal from Azure portal"
    infoBubbleText="Problems related to network issues within the Private Cloud VMs"
    ms.service="azure-vmware-cloudsimple"
    authors="dikamath, sharaths-cs" 
    ms.author="dikamath, b-shsury, v-rabmah"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32637629"
    resourceTags=""
    productPesIds="16733"
    cloudEnvironments="public, fairfax, usnat, ussec" 
    articleId="34600d96-683e-4909-84e6-a87d888f9cb9"    
	ownershipId="Compute_VirtualMachines_Content"
/>

# Troubleshooting network connectivity between VMs 

## **Recommended Steps**

* Check if there are firewall rules blocking any outbound traffic
* Check the VM network configuration: IP address, subnet mask and gateway 
* Check if the VM is attached to correct distributed port group 
* Check if the distributed port group has correct VLAN ID 
* If you are in connection to on-premises VM, check the ExpressRoute connection 


## **Recommended Documents**

<span title="Problems related to network issues within the Private Cloud VMs">

* [Use VLAN Information to Set Up a Distributed Port Group in vSphere](https://docs.microsoft.com/azure/vmware-cloudsimple/create-vlan-subnet#use-vlan-information-to-set-up-a-distributed-port-group-in-vsphere)<br>
</span>

<span title="Problems related to network issues within the Private Cloud VMs">

* [Firewall Rules](https://docs.microsoft.com/azure/vmware-cloudsimple/firewall#firewall-rules)<br>
</span>

<span title="Problems related to network issues within the Private Cloud VMs">

* [VLANs/Subnets](https://docs.microsoft.com/azure/vmware-cloudsimple/create-vlan-subnet)<br>
</span>