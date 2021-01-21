<properties
	  pageTitle="Add source IP to JIT Policy"
	  description="Add source IP to JIT Policy"
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
	  articleId="a25085cf-4e23-4c1d-b3e5-65cb17c90f4f"
	  ownershipId="Azure_Security_Security_Center"
/>

# Add source IP to JIT Policy

<!--issueDescription-->

Based on the troubleshooting done so far we have found the following, we have found that your source IP is out of JIT policy range. Add the source IP address (The VM you are connecting from) to the JIT policy IP address range or request the access using Resource IP = Any (*). Please add the IP to the JIT Policy using the article [Add Source IP to JIT Policy Range](https://docs.microsoft.com/azure/security-center/security-center-just-in-time?tabs=jit-config-asc%2Cjit-request-asc#enable-jit-vm-access-)
<br>

<!--/issueDescription-->