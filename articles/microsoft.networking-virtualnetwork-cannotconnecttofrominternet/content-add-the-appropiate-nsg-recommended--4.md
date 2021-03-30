<properties
	  pageTitle="Add the appropiate NSG recommended "
	  description="Add the appropiate NSG recommended "
      service="Microsoft.network"
      resource="Microsoft.Network/virtualNetworks"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="b4e823c8-dceb-431f-9a1c-bafdd8824beb"
	  ownershipId="Centennial_Cloudnet_virtualNetwork"
/>

# Add the appropiate NSG recommended 

"The SKU of the VIP will if incoming traffic is allowed or denied by default. 


## Recommended Steps 

1. Navigate to the VM in ASC Resource Explorer
2.  From the Properties select ""IP Configurations""
3. If a public IP exist select it.
4. Once the IP information loads you will find the SKU in the ""Properties"" section

If Standard Sku:
- IPs are secure and closed to inbound traffic. Allow list inbound traffic with an NSG

If Basic SKU:

- IPs are open by default, with that, ensure the necessary outgoing traffic. Please check at the Nic level as well as at the subnet level

#Reccommended Documents

1.(VIP SKUs)[https://docs.microsoft.com/en-us/azure/virtual-network/public-ip-addresses#sku]"

