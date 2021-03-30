<properties
	  pageTitle="Attach the VM to a NIC/NSG"
	  description="Attach the VM to a NIC/NSG"
      service="Microsoft.Compute"
      resource="Microsoft.Compute/virtualMachines,Microsoft.Compute/virtualMachineScaleSets"
	  authors="rimayber"
	  ms.author="rimayber"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="67f1363b-839e-4bb6-988a-3276d133d027"
	  ownershipId="Azure_Security_Security_Center"
/>

# Attach the VM to a NIC/NSG

<!--issueDescription-->

JIT operates by creating Allow and Deny rules to the NSG. <br>
All VMs Networking must have both in order to be protected be Security Center JIT.<br>
Please attach them as descriibed in the article [NSG Overview](https://docs.microsoft.com/azure/virtual-network/network-security-groups-overview)<br>

<!--/issueDescription-->
