<properties
	  pageTitle="JIT Policy doesn't seems to be configured"
	  description="JIT Policy doesn't seems to be configured"
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
	  articleId="db1d092e-af99-41d2-97e1-fde8203fc0f4"
	  ownershipId="Azure_Security_Security_Center"
/>

# JIT Policy doesn't seems to be configured

<!--issueDescription-->

Dear Customer,<br>

The user probably does not have authorization to perform the needed action.<br>
<br>
Check that the role assignment contains this action:<br>
 'Microsoft.Security/locations/jitNetworkAccessPolicies/write' over scope subscriptions/jitNetworkAccessPolicies.<br>
<br>
The user should have the RBAC role to contain the above actions (Contributor or Owner) as described here in the link below. <br>
Best Regards,<br>

<!--/issueDescription-->

## Recommended Documents

1. [Understanding just-in-time virtual machine access in Azure Security Center](https://docs.microsoft.com/en-us/azure/security-center/just-in-time-explained)