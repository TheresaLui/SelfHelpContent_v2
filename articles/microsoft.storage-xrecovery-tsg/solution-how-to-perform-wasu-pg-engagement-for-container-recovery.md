<properties
	pageTitle="How to perform WASU PG engagement for container recovery"
	description="How to perform WASU PG engagement for container recovery"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="symondsk"
	ms.author="ksymonds"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	ownershipId="StorageMediaEdge_AccountManagement"
	articleId="b9dd5a07-bbfe-460c-8cb0-e5260253e3f0"
/>

# File an IcM for container recovery

<!--issueDescription-->

Recovery may be possible or the previous procedure was not possible due to an issue, please proceed with engaging XStore/Location Service team. If you don't have access to route the ICM to XStore/Location service team, engage one of the storage TAs or email [cssstorageta@microsoft.com](mailto:cssstorageta@microsoft.com).
</br>

1. Check if the Storage Account type is LRS, if yes, reply to customer that recovery of the container is not possible

2. If the Storage is GRS ask the customer to make it RA-GRS type.

3. Ask the customer to create a SAS token that is needed for the recovery purposes.

```powershell
$storageAccount = "<name>"
$storageKey = "<key>"
$ctx = New-AzureStorageContext –StorageAccountName $storageAccount -StorageAccountKey $storageKey
$startTime = Get-Date
$endTime = $startTime.AddMonths(1)
New-AzureStorageContainerSASToken -Name "<containerName>" -Permission rl -StartTime $startTime -ExpiryTime $endTime -Context $ctx -FullUri
```

Or if the customer has deleted multiple containers you can use the script below:<br>


```powershell
$containername = @(Get-Content "<path on local machine for a .csv or .txt file with the list of containers>")
$storageAccount = "<storage account name>"
$storageKey = "<Access key>"
$ctx = New-AzureStorageContext –StorageAccountName $storageAccount -StorageAccountKey $storageKey
$startTime = Get-Date
$endTime = $startTime.AddMonths(1)
$containername.foreach{New-AzureStorageContainerSASToken -Name "$PSItem" -Permission rl -StartTime $startTime -ExpiryTime $endTime -Context $ctx -FullUri}
```

4. Gather the SAS Token and store it securely. Do not share it with anybody until required. Please see below guidance for more information. <br>

5. Create a Sev 3 [ICM](https://portal.microsofticm.com/imp/v3/incidents/create?tmpl=l1sW2L) to [XStore/Location Service](https://portal.microsofticm.com/imp/v3/incidents/create?tmpl=l1sW2L) and provide only the Storage Account details and recovery request. ***DO NOT INCLUDE THE SAS TOKEN IN THE ICM DETAILS.*** SAS Token must be shared only with the XStore Location service [On-call Primary contact](https://portal.microsofticm.com/imp/v3/oncall/current?serviceId=10050&teamIds=11196&scheduleType=current&shiftType=current&viewType=1&gridViewStartDate=2020-11-25T08%3A00%3A00.000Z&gridViewEndDate=2020-12-01T08%3A00%3A00.000Z&gridViewSelectedDateRangeType=4) who will perform the recovery operation.<br>

6. Once the responsible team on-call engineer is engaged, proceed to share the Customer's SAS token collected earlier in a private communication to that person.

<!--/issueDescription-->