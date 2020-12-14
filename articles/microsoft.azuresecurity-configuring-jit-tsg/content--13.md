<properties
	  pageTitle="Check if the JIT allow rule is the highest priority in the NSG"
	  description="Check if the JIT allow rule is the highest priority in the NSG"
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
	  articleId="169877e8-0c30-423c-8897-25c6d5bcf897"
	  ownershipId="Azure_Security_Security_Center"
/>

# Check if the JIT allow rule is the highest priority in the NSG

1. Check the NSG for JIT Rules.
2. Go to VM -> Networking -> Inbound port rule.
3. When JIT access request initiated it create an Allow rule on the higest priority (100-140), carrying the following naming convention: *SecurityCenter-JITRule-xxxxxxx-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx*"
