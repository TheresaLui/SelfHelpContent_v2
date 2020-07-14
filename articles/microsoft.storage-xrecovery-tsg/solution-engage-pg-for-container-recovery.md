<properties
	pageTitle="How to perform WASU/PG engagement for container recovery"
	description="How to perform WASU/PG engagement for container recovery"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	ownershipId="Centennial_CloudNet_LoadBalancer"
	articleId="a0a2ad09-3438-45f8-99ac-87a23b1b089b"
/>

# How to perform WASU/PG engagement for container recovery

<!--issueDescription-->
1. If storage account does not have Read Access to secondary, customer will need to change it to RA-GRS or RA-GZRS for recovery attempt.<br>
2. Have the customer create a SAS token that will be needed for the recovery purposes. Here is the powershell command.<br>
3. **NOTE** : Do **NOT** include this in the IcM or in notes. Only provide this to the WASU or XStore engineer on request.<br>

~~~powershell

$storageAccount = "$name$"
$storageKey = "$key$"
$ctx = New-AzureStorageContext –StorageAccountName $storageAccount -StorageAccountKey $storageKey
$startTime = Get-Date
$endTime = $startTime.AddMonths(1)
New-AzureStorageContainerSASToken -Name "$containerName$" -Permission rl -StartTime $startTime -ExpiryTime $endTime -Context $ctx -FullUri

~~~

4. Create a Sev 2 ICM to WASU (or a Sev 3 to XStore PG) and provide only the Storage Account details and recovery request. Again, do NOT include the SAS Token in the ICM details. SAS Token must be shared only with the WASU/XStore engineer who will perform the recovery operation.<br>
5. Once the responsible team on-call engineer is engaged, proceed to share the Customer's SAS token collected earlier in a private communication to that person.<br>

<!--/issueDescription-->