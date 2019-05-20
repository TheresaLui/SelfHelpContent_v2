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
Failed to enable replication, as virtual machine is not in desired state.
<!--/issueDescription-->

## **Recommended Steps**

To enable replication on the VM, the provisioning state should be succeeded. To resolve this issue, make sure that the virtual machine provisioning state is Succeeded. Then retry the operation. For more information, see [VM's provisioning state is not valid (error code 150019)](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-errors#vms-provisioning-state-is-not-valid-error-code-150019).

