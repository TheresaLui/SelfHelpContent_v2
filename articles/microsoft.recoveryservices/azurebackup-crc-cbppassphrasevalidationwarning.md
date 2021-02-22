<properties
	pageTitle="CBPPassphraseValidationWarning"
	description="CBPPassphraseValidationWarning"
	infoBubbleText="encryption passphrase has not been validated to meet requirements"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-cbppassphrasevalidationwarning"
	diagnosticScenario="azurebackup-crc-cbppassphrasevalidationwarning"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error CBPPassphraseValidationWarning

<!--issueDescription-->
We have identified that you have MARS jobs which are succeeding but generating the warning CBPPassphraseValidationWarning. This warning is generated on job completion once a week as a reminder that the encryption passphrase has not been validated to meet requirements. This is critical to ensure successful restores so Microsoft recommends that the passphrase be validated at the earliest. Once the validation is successful, the warnings will no longer be generated.
<!--/issueDescription-->

## **Recommended Steps**

1.	Launch the MARS agent console and click on the *Validate* link on the message that shows up at the top of the console. 
OR
Alternatively, search for the validator executable *PassphraseValidator.exe* and launch it from an elevated command prompt window
2.	Provide the current passphrase. This will be validated both for correctness and to ensure it meets requirements
3.	If the passphrase provided is incorrect (forgotten or mistaken entry) the option to [regenerate the passphrase](https://docs.microsoft.com/azure/backup/backup-azure-manage-mars#re-generate-passphrase) is provided. <br>NOTE: A Security PIN needs to be generated from the azure portal to complete this step
4.	The passphrase that is set is written out to a text file. Please save this in a secure location preferably outside of the machine so that it will be available when needed for restore

Recommended Documentation
-	[Mandatory Update for Azure Backup for Microsoft Azure Recovery Services Agent](https://support.microsoft.com/help/4575948/mandatory-update-for-azure-backup-for-microsoft-azure-recovery-service)
