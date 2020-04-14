<properties
    pageTitle="Access Azure VMware Solution by CloudSimple - Portal" 
    description="Describes how to access VMware Solution by CloudSimple portal from Azure portal"
    infoBubbleText="Problems related to configured firewall rules and associated subnets, IPs, Public IP addresses"
    ms.service="azure-vmware-cloudsimple"
    authors="dikamath, sharaths-cs" 
    ms.author="dikamath, b-shsury, v-rabmah"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32637583"
    resourceTags=""
    productPesIds="16733"
    cloudEnvironments="public, fairfax, usnat, ussec" 
    articleId="8e16284c-b286-49aa-9e37-28219d677f74"    
	ownershipId="Compute_VirtualMachines_Content"
/>

# Troubleshooting firewall table and rules 

## **Recommended Steps**

* Check if the firewall table is attached to the correct subnet
* Check if the firewall rules are configured on firewall table
* Check that the virtual machine is using the correct distributed port group
* If you are using NSX Distributed Firewall, check if the firewall rules are correctly configured
* If you are using NSX Distributed Firewall, check if the firewall rules are in the correct sequence
* If you are using NSX Distributed Firewall, check if the **Applied to** field of the firewall rule is correct


## **Recommended Documents**

<span title="Problems related to configured firewall rules and associated subnets, IPs, Public IP addresses">

* [Firewall Table](https://docs.microsoft.com/azure/vmware-cloudsimple/firewall#add-a-new-firewall-table)<br>
</span>

<span title="Problems related to configured firewall rules and associated subnets, IPs, Public IP addresses">

* [Firewall Rules](https://docs.microsoft.com/azure/vmware-cloudsimple/firewall#firewall-rules)<br>
</span>
