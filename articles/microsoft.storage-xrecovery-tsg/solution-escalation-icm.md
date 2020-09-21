<properties
	pageTitle="Escalation File an IcM"
	description="Escalation File an IcM"
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
	articleId="edef6e58-e0be-463a-8a41-c8172fee2f4c"
/>

# Escalation File an IcM

<!--issueDescription-->

1. Have customer create a SAS token that will be needed for recovery purposes.<br> 
2. Here is the powershell command. NOTE : Do NOT include the SAS URL in the IcM or in notes. Only provide this to the WASU or XStore engineer on request.<br>
3. Recommended sample command Steps:<br>

~~~powershell

$storageAccount = ""
$storageKey = ""
$ctx = New-AzureStorageContext –StorageAccountName $storageAccount -StorageAccountKey $storageKey
$startTime = Get-Date
$endTime = $startTime.AddMonths(1)
New-AzureStorageTableSASToken -Name "" -Permission rl -StartTime $startTime -ExpiryTime $endTime -Context $ctx -FullUri

~~~

4. File the IcM to check for recovery options. <br>
5. Choose an ICM Template based on severity and include all deletion information gathered in previous steps<br>

## Recommended Documents
1. [Sample Sev 2 IcM to WASU](https://portal.microsofticm.com/imp/v3/incidents/create?tmpl=v154BG)
2. [Sample Sev 3 IcM](https://aka.ms/IcMXTableServer)
<!--/issueDescription-->