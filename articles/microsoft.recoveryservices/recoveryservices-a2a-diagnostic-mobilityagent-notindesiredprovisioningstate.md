<properties
	pageTitle="Microsoft Azure has information regarding your issue"
	description="Microsoft Azure has information regarding your issue"
	infoBubbleText="Microsoft Azure has information regarding your issue. Please see details on the right."
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="genlin"
	ms.author="asgang"
	displayOrder=""
	articleId="ASR_A2A_EnableReplicationFailure_AzureVmIsNotInDesiredProvisioningState"
	diagnosticScenario="ASRA2AMgmtFailures"
	selfHelpType="Diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Enable replication failed as virtual machine is not in desired state
<!--issueDescription-->
Fail to enable replication because the virtual machine is not running.
<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue, restart the virtual machine, and then retry the operation. If the provisioning state is **Updating**, check if there are any ongoing operations on the virtual machine, and wait for them to complete, and then retry the replication.

## **Recommended Documents**

* [Virtual machine's provisioning state is not valid (error code 150019)](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-errors#vms-provisioning-state-is-not-valid-error-code-150019)

