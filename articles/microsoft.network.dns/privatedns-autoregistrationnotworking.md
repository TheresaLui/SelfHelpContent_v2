<properties 
    pageTitle="Auto-registration of VM records is not working"
    description="DNS records for virtual machines are not automatically populated in the private DNS zone"
    service="microsoft.network"
    resource="privateDnsZones"
    authors="rohinkoul"
    ms.author="rohink"
    displayOrder="4"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public,fairfax,mooncake,blackforest, usnat, ussec"
	articleId="privatedns-autoregistrationnotworking"
	ownershipId="CloudNet_DNS"
/>

# Auto-registration of VM records is not working

## **Recommended Steps**

To resolve common issues, try one or more of the following:

* Confirm that virtual network is linked to the private DNS zones and registration is enabled:

  * Go to the "virtual network links" tab on the private DNS zone resource blade in the Azure portal
  * You'll see list of all virtual network links associated with the zone. In case the virtual network link for your virtual network is not listed, create a new virtual network link for your virtual network and ensure that registration flag is enabled.
  * In case you see the virtual network link for your virtual network, ensure that registration flag on it is enabled. If registration is not enabled, click on the link and check the checkbox for enabling auto registration and save the link configuration.

* Try restarting the virtual machines or refreshing DHCP lease on the virtual machines. This will refresh the DNS record in the private DNS zone.
* Auto registration works only for primary NIC of the virtual machine. If you have virtual machines with more than one NIC, you must manually create DNS records for other NICs of the virtual machine.
