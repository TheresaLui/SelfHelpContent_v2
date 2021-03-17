<properties
	pageTitle="UserErrorHANASystemDBNotRunning"
	description="UserErrorHANASystemDBNotRunning"
	infoBubbleText="SYSTEMDB for HANA is not in running state"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorhanasystemdbnotrunning"
	diagnosticScenario="azurebackup-crc-usererrorhanasystemdbnotrunning"
	selfHelpType="diagnostics"
	supportTopicIds=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# UserErrorHANASystemDBNotRunning 

<!--issueDescription-->
We have identified that your backup operation failed because SYSTEMDB for SAP HANA instance is not in running state.
<!--/issueDescription-->

## **Recommended Steps**

- Ensure SystemDB for the SAP HANA instance is in running state. Start the SAP HANA system by running the command `HDB start` as the *sidadm* user and retry the operation
- After executing the `HDB start` command check if the process state of each service for the DB is healthy using the command `sapcontrol -nr \<instance number> function GetProcessList`
