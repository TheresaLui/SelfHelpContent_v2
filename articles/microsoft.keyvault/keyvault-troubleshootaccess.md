<properties
  pagetitle="Troubleshoot Access to Key Vault&#xD;"
  service="microsoft.keyvault"
  resource="vaults"
  ms.author="jalichwa,sebansal"
  selfhelptype="Generic"
  supporttopicids="32743816"
  resourcetags="optional"
  productpesids="15657"
  cloudenvironments="blackforest,fairfax,public,mooncake,usnat,ussec"
  articleid="keyvault-troubleshootaccess"
  ownershipid="AzureKeyVault_KeyVault" />
# Troubleshoot Access to Key Vault

## **Recommended Steps**

* See [answers to questions about issues related to access to Key Vault](https://docs.microsoft.com/azure/key-vault/general/troubleshooting-access-issues), which covers issues such as unable to add access, unknown access policy, and not able to access to Key Vault.  

* If you have issues authenticating to Key Vault in code, use [Authentication SDK](https://docs.microsoft.com/azure/key-vault/general/developers-guide#coding-with-key-vault).

### **Troubleshooting**

#### **Troubleshooting Intermittent Failures**
* Security Group Access Policy Configuration - See [Troubleshooting steps]( https://docs.microsoft.com/azure/key-vault/general/group-permissions-for-apps#azure-ad-groups)


#### **Troubleshooting Error Codes**
* HTTP 401: Unauthenticated Request - See [Troubleshooting steps](https://docs.microsoft.com/azure/key-vault/general/rest-error-codes#http-401-unauthenticated-request)
* HTTP 403: Insufficient Permissions - See [Troubleshooting steps](https://docs.microsoft.com/azure/key-vault/general/rest-error-codes#http-403-insufficient-permissions)
* HTTP 429: Too Many Requests - See [Troubleshooting steps](https://docs.microsoft.com/azure/key-vault/general/rest-error-codes#http-429-too-many-requests)

#### **Troubleshooting Private Link Connection**

* Check to make sure the private endpoint is in the Approved state:

	* You can check and fix this in Azure portal. Open the Key Vault resource, and click the Networking option.
	* Select the Private Endpoint connections tab
	* Make sure connection state is Approved and provisioning state is Succeeded
	* You may also navigate to the private endpoint resource and review same properties there, and double-check that the virtual network matches the one that you are using

* Check to make sure you have a Private DNS Zone resource:

	* You must have a Private DNS Zone resource with the exact name: privatelink.vaultcore.azure.net
	* To learn how to set this up, see [Private DNS Zones](https://docs.microsoft.com/azure/dns/private-dns-privatednszone)
    
* Check to make sure the Private DNS Zone is not linked to the Virtual Network. This may be the issue if you are still getting the public IP address returned:

	* If the Private Zone DNS is not linked to the virtual network, the DNS query originating from the virtual network will return the public IP address of the key vault
	* Navigate to the Private DNS Zone resource in the Azure portal and click the virtual network links option
	* The virtual network that will perform calls to the key vault must be listed
	* If it's not there, [add it](https://docs.microsoft.com/azure/dns/private-dns-getstarted-portal#link-the-virtual-network)

* Check to make sure the Private DNS Zone is not missing an A record for the key vault:

	* Navigate to the Private DNS Zone page
	* Click **Overview** and check if there is an A record with the simple name of your key vault (for example, fabrikam). Do not specify any suffix.
	* Make sure you check the spelling, and either create or fix the A record. You can use a TTL of 3600 (1 hour). 
	* Make sure you specify the correct private IP address
    
* Check to make sure the A record has the correct IP Address:

	* You can confirm the IP address by opening the Private Endpoint resource in Azure portal 
	* Navigate to the Microsoft.Network/privateEndpoints resource, in the Azure portal (not the Key Vault resource)
	* In the overview page look for Network interface and click that link
	* The link will show the Overview of the NIC resource, which contains the property Private IP address
	* Verify that this is the correct IP address that is specified in the A record

## **Recommended Documents**

* For roles that you can use to grant access to Azure resources, see [List of Azure Role Definitions](https://docs.microsoft.com/azure/role-based-access-control/role-definitions-list)
* [Authenticate to Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/authentication)
* [Grant access to Key Vault with Access Policies](https://docs.microsoft.com/azure/key-vault/general/assign-access-policy-portal)
* [Grant access to Key Vault with Azure Roles](https://docs.microsoft.com/azure/key-vault/general/rbac-guide)
