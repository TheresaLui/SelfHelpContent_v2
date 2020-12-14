<properties
	  pageTitle="Permissions for enabling JIT"
	  description="Permissions for enabling JIT"
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
	  articleId="021ed202-8671-4248-91ba-aacc9c144ec5"
	  ownershipId="Azure_Security_Security_Center"
/>

# Permissions for enabling JIT

1. Check that the role assignment contains this action:
2. 'Microsoft.Security/locations/jitNetworkAccessPolicies/write' over scope subscriptions/jitNetworkAccessPolicies.
3. Customer should have the RBAC role to contain the above actions (Contributor or Owner) as described at [Understanding just-in-time virtual machine access in Azure Security Center](https://docs.microsoft.com/azure/security-center/just-in-time-explained)
