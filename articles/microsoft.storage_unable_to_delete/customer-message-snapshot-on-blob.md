<properties
	pageTitle="Delete snapshots to delete blob"
	description="Delete snapshots to delete blob"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="b41f8eed-d7fb-4db0-bd55-7fb79b6c228a"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Delete snapshots to delete blob
<!--issueDescription-->
We've reviewed your case and believe the issue is due to the existence of a snapshot of a virtual machine disk within the blob. Snapshots are not visible in the portal. In order to delete the blob, you must first delete the snapshots. 
<!--/issueDescription-->

## **Recommended Steps**

Below is an example of a powershell command to delete a blobs snapshot:

1. Set the parameters:

```
$ResourceGroupName = 'resourcegroupname'
$StorageAccountName = 'storageaccountname'
$ContainerName = 'vhds'
$BlobFilename = 'blobfilename.vhd'
```

2. Login to ARM: `Login-AzureRmAccount`

3. Set the storage context:

```
$storageAccountKey = Get-AzureRmStorageAccountKey -Name $StorageAccountName -ResourceGroupName $ResourceGroupName
$storageContext = New-AzureStorageContext -StorageAccountName $StorageAccountName -StorageAccountKey $storageAccountKey[0].Value
```

4. Get all blobs with a name like $BlobFilename, and filter them to those that are snapshots for $BlobFilename:

```
$blobSnapshots = Get-AzureStorageBlob –Context $storageContext -Prefix $BlobFilename -Container $ContainerName | Where-Object {$_.ICloudBlob.IsSnapshot -and $_.Name -eq $BlobFilename -and $_.SnapshotTime -ne $null }
```

5. Loop through all of the snapshots, and delete each one:

```
foreach ($blobSnapshot in $blobSnapshots)
{
    $blobSnapshot.ICloudBlob.Delete()
}
```
