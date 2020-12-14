<properties
	  pageTitle="Check if JIT Configured on the VM NSG"
	  description="Check if JIT Configured on the VM NSG"
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
	  articleId="e9dd5f69-16b3-4eb7-95a5-2b9e05ca00e3"
	  ownershipId="Azure_Security_Security_Center"
/>

# Check if JIT Configured on the VM NSG

1. Check the NSG for JIT Rules.
2. Go to VM -> Networking -> Inbound port rule.
3. When JIT policy is first configured, it creates a low priority (> 1000) Deny rule per IP Address/ports, carrying the following naming convention: *SecurityCenter-JITRule_-xxxxxxx-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx*
4. If does not exist it means that JIT was not configured.
5. Please ask customer to configure JIT policy on the VM.