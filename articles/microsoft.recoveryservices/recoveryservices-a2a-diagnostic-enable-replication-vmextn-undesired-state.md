<properties
    pageTitle="Enable replication failed as task execution has timed out while tracking for extension operation to be started"
    description="Task execution has timed out while tracking for extension operation to be started as Azure guest agent is not in the desired state"
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_A2A_EnableReplicationFailure_VmExtnOpNotStartedUndesiredGAState"
    diagnosticScenario="ASRA2AMgmtFailures"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Enable replication failed as agent is not in desired state

<!--issueDescription-->
When you enable replication for a Azure VM, it fails with error "Task execution has timed out while tracking for extension operation to be started". This occurs because Azure guest agent is not in the desired state.
<!--/issueDescription-->

## **Recommended Steps**

Verify the Azure VM agent status is Ready. To do that, follow these steps:

- In Azure portal, go to the VM that is experiencing this failure
- Select **Settings**, select **Properties**, then select **Agent status**

## **Recommended Documents**

- For more information, see [Troubleshoot issues with the Azure Site Recovery agent](https://docs.microsoft.com/azure/site-recovery/site-recovery-extension-troubleshoot#protection-fails-because-the-vm-agent-is-unresponsive)
