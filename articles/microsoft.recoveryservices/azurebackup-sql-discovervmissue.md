<properties
		pageTitle="Azure Backup unable to discover VM"
		description="Azure Backup SQL Config failures"
		service="microsoft.recoveryservices"
		resource="vaults"
		authors="srinathv"
		ms.author="srinathv"
		displayOrder=""
		selfHelpType="generic"
		supportTopicIds="32632804"
		resourceTags=""
		productPesIds="15207"
		cloudEnvironments="public, fairfax, usnat, ussec"
		articleId="91077485-46e3-4c9f-a5ae-6d71eae1cf85"
	ownershipId="StorageMediaEdge_Backup"
/>
# Azure Backup SQL Config failures

## **Recommended Steps**

- **VMNotInRunningStateUserError**: [Ensure the SQL Server is running](https://aka.ms/AA4f1h6)</br>
- **FabricSvcBackupPreferenceCheckFailedUserError**: [Backup preference for SQL Always On Availability Group cannot be met as some nodes of the Availability Group are not registered](https://aka.ms/AB-fabricsvcbackuppreferencecheckfailedusererror)<br>
- **VMNotInRunningStateUserError**: [SQL server VM is either shutdown and not accessible to Azure Backup service](https://aka.ms/AB-vmnotinrunningstateusererror)<br>
- **GuestAgentStatusUnavailableUserError**: [Azure Backup service uses Azure VM guest agent for doing backup but guest agent is not available on the target server](https://aka.ms/AB-guestagentstatusunavailableusererror)<br>
- **AutoProtectionCancelledOrNotValid**: [Auto-protection Intent was either removed or is no longer valid](https://aka.ms/AB-autoprotectioncancelledornotvalid)
- [Can I throttle the speed of the SQL Server backup policy?](https://aka.ms/AB-AA4dp5n) </br>
- [When I protect a SQL Server instance are future databases automatically added?](https://aka.ms/AB-AA4dp5q)</br>
- [If I change the recovery model, how do I restart protection?](https://aka.ms/AB-AA4dp5p)</br>
- [Can I protect SQL Always On Availability Groups where the primary replica is on premises?](https://aka.ms/AB-AA4dwue)</br>

## **Recommended Documents**

- [Frequently asked questions](https://aka.ms/AB-AA4dwuc)</br>
- [Troubleshooting issues related to back up SQL Server to Azure](https://aka.ms/AB-AA4dwud)</br>
