<properties
    pageTitle="Volume encryption needs to be enabled for target Key Vault"
    description="Volume encryption needs to be enabled for target Key Vault."
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_A2A_VirtualMachineCreationFailure-KeyVaultVolumeEncryptionNotEnabled"
    diagnosticScenario="ASRA2AMgmtFailures"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Volume encryption needs to be enabled for target Key Vault

<!--issueDescription-->
Azure Site Recovery is not able to create a failed over virtual machine in Azure. You may receive an error message that resembles the following:

"Failover Error: ID28031 Error Message: Virtual machine 'virtual machine name' could not be created under resource group 'resource group name'. Azure error message: 'Key Vault https://xx.vault.azure.net/secrets/xx/xx either has not been enabled for Volume Encryption or the vault id provided does not match /subscriptions/xx/resourceGroups/xx/providers/Microsoft.KeyVault/vaults/xx's true resource id. (Provisioning failed)'."
<!--/issueDescription-->

## **Recommended Steps**

Verify the volume encryption is enabled in target Key Vault. To do that, follow these steps:

- In Azure portal, locate the target Key Vault
- In the vault, select **Access polices**
- If **Azure Disk Encryption for volume encryption** is not checked, check it and save the changes

## **Recommended Documents**

- For more information, see [Troubleshoot failover to Azure](https://docs.microsoft.com/azure/site-recovery/site-recovery-failover-to-azure-troubleshoot#failover-failed-with-error-id-28031)
