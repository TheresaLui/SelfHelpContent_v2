<properties
	pageTitle="Microsoft Azure has information regarding your issue"
	description="Microsoft Azure has information regarding your issue"
	infoBubbleText="Microsoft Azure has information regarding your issue. Please see details to the right."
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="genlin"
	ms.author="asgang"
	displayOrder=""
	articleId="AzureVmIsNotInDesiredProvisioningState"
	diagnosticScenario="AzureVmIsNotInDesiredProvisioningState"
	selfHelpType="Diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="Public"
/>

# Enable replication failed as virtual machine is not in desired state
<!--issueDescription-->
Failed to enable replication, because the virtual machine is not in a state to replicate.
<!--/issueDescription-->

## **Recommended Steps**

 To resolve this issue, make sure that the virtual machine provisioning state is **Succeeded**, and then retry the operation. If provisioning state is **Updating**, check if there are any ongoing operations on the virtual machine, wait for them to complete, and then retry the replication job. For more information, see [virtual machine's provisioning state is not valid (error code 150019)](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-errors#vms-provisioning-state-is-not-valid-error-code-150019).

