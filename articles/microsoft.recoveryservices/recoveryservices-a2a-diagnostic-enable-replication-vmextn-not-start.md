<properties
    pageTitle="Task execution has timed out while tracking for extension operation to be started"
    description="Enable replication failed as task execution has timed out while tracking for extension operation to be started"
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_A2A_EnableReplicationFailure_VmExtnOpNotStarted"
    diagnosticScenario="ASRA2AMgmtFailures"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Enable replication failed as extension operation is not started

<!--issueDescription-->
When you enable replication for a Azure VM, it fails with error "Task execution has timed out while tracking for extension operation to be started". This occurs because extension operation is not started by Azure VM agent.
<!--/issueDescription-->

## **Recommended Steps**

Verify the site recovery extension status on the VM and retry the operation.

- For a VM running Windows OS, try restarting Windows Azure guest agent service in the VM
- For a VM running Linux OS, try restarting Linux Azure guest agent service and ensure that the agent version is the latest version

## **Recommended Documents**

- For more information, see [Troubleshoot issues with the Azure Site Recovery agent](https://docs.microsoft.com/azure/site-recovery/site-recovery-extension-troubleshoot#azure-site-recovery-extension-time-out)
