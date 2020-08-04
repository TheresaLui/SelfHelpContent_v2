<properties
	pageTitle="Azure Key Vault Configure Private Link Connection"
	description="Azure Key Vault Configure Private Link Connection"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="ShaneBala-keyvault"
	ms.author="sudbalas"
	displayOrder="9"
	selfHelpType="generic"
	supportTopicIds="32743814"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="keyvault-configureprivatelinkconnection"
	ownershipId="AzureKeyVault_KeyVault"
/>

# Azure Key Vault Access Policies and Security Groups

## **Recommended Steps**

* Check to make sure the private endpoint is in the approved state:

	* You can check and fix this in Azure portal. Open the Key Vault resource, and click the Networking option.
	* Select the Private endpoint connections tab
	* Make sure connection state is Approved and provisioning state is Succeeded
	* You may also navigate to the private endpoint resource and review same properties there, and double-check that the virtual network matches the one you are using

* Check to make sure you have a Private DNS Zone resource:

	* You must have a Private DNS Zone resource with the exact name: privatelink.vaultcore.azure.net
	* To learn how to set this up please [Private DNS Zones](https://docs.microsoft.com/azure/dns/private-dns-privatednszone)
    
* Check to make sure the Private DNS Zone is not linked to the Virtual Network. This may be the issue if you are still getting the public IP address returned:

	* If the Private Zone DNS is not linked to the virtual network, the DNS query originating from the virtual network will return the public IP address of the key vault
	* Navigate to the Private DNS Zone resource in the Azure portal and click the virtual network links option
	* The virtual network that will perform calls to the key vault must be listed
	* If it's not there, [add it](https://docs.microsoft.com/azure/dns/private-dns-getstarted-portal#link-the-virtual-network)

* Check to make sure the Private DNS Zone is not missing an A record for the key vault:

	* Navigate to the Private DNS Zone page
	* Click Overview and check if there is an A record with the simple name of your key vault (i.e. fabrikam). Do not specify any suffix.
	* Make sure you check the spelling, and either create or fix the A record. You can use a TTL of 3600 (1 hour). 
	* Make sure you specify the correct private IP address
    
* Check to make sure the A record has the correct IP Address:

	* You can confirm the IP address by opening the Private Endpoint resource in Azure portal 
	* Navigate to the Microsoft.Network/privateEndpoints resource, in the Azure portal (not the Key Vault resource)
	* In the overview page look for Network interface and click that link
	* The link will show the Overview of the NIC resource, which contains the property Private IP address
	* Verify that this is the correct IP address that is specified in the A record
	
## **Recommended Documents**

* [Integrate Key Vault with Azure Private Link](https://docs.microsoft.com/azure/key-vault/general/private-link-service)
* [Azure Private Link Overview](https://docs.microsoft.com/azure/private-link/private-link-overview)
* [Azure Private Endpoint Overview](https://docs.microsoft.com/azure/private-link/private-endpoint-overview)

