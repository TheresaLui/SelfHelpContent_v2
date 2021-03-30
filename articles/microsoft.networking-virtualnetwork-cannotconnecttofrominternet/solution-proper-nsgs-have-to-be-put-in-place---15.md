<properties
	  pageTitle="Proper NSGs have to be put in place. "
	  description="Proper NSGs have to be put in place. "
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
	  articleId="bd137835-0849-4025-bee7-762d023cbb4c"
	  ownershipId="Centennial_Cloudnet_virtualNetwork"
/>

# Proper NSGs have to be put in place. 

<!--issueDescription-->

<!--issueDescription-->
Our investigation has determined that the Proper NSGs have to exist

If Standard Sku:
- IPs are secure and closed to inbound traffic. Allow desired inbound traffic with an NSG uncluding <destination IP> <Port>

If Basic SKU:

- IPs are open by default, with that, ensure the necessary inbound and outbound traffic is being allowed, uncluding <destination IP> <Port>
<!--/issueDescription-->"

<!--/issueDescription-->

