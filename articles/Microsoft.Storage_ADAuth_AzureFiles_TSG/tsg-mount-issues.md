<properties
    pageTitle="Customer is facing issues while mounting the file share."
    description="Customer is facing issues while mounting the file share."
    service="microsoft.storage"
    resource="storageAccounts"
    authors="yagohel23"
    ms.author="yagohel"
    displayOrder=""
    selfHelpType="TSG_Content"
    supportTopicIds="32689882"
    resourceTags=""
    productPesIds="1003478"
    cloudEnvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
    articleId="22055eb3-34cb-4f87-97da-dd62352a501d"
    ownershipID="StorageMediaEdge_StorageFiles"
/>

# Customer is facing issues while mounting the file share

The following section of the TSG will help you troubleshoot mount issues for a particular file share.

Before you go to next step, make sure the customer is trying to mount the file share using the "net use" command as explained [here](https://docs.microsoft.com/azure/storage/files/storage-files-identity-auth-active-directory-enable#4-mount-a-file-share-from-a-domain-joined-vm).

## Private Endpoint scenario

In a scenario where the customer has Private Endpoint setup for Azure Files, make sure they are trying to mount using the "*.file.core.windows.net" storage endpoint and not using the "privatelink" subdomain URL. For more details, see [here](https://docs.microsoft.com/azure/storage/common/storage-private-endpoints#connecting-to-private-endpoints)

Also, make sure the customer sees Private IP assigned to the Private Link resource when they do nslookup on the file storage endpoint. For more details, see this [TSG](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/280935/Azure-Storage-Private-Endpoints?anchor=check-if-the-customer-has-appropriate-dns-config-in-place).

## Mount File Share using Storage Account Key

Once you have verified that the customer does not have Private Endpoint enabled or has their Private Endpoint setup successfully, try and see if they are able to mount the file share using the storage account key. If mount fails, please have them run [AzFileDiagnostics.ps1](https://github.com/Azure-Samples/azure-files-samples/tree/master/AzFileDiagnostics) to validate any client side issues and help them resolve those issues as needed. Use this [TSG](https://centennialtsg.azurewebsites.net/TSG2/123931) if required.

## Use "Debug-AzStorageAccountAuth" command to further isolate the issue

Once you have confirmed that the user is able to mount the file share using the storage account key but cannot map the same share using their On-Prem credential, use [Debug-AzStorageAccountAuth cmdlet](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#self-diagnostics-steps) (with "-Verbose" option) to further isolate the issue. This cmdlet is supported on [AzFilesHybrid v0.1.2+ version and above](https://github.com/Azure-Samples/azure-files-samples/releases). You need to run this cmdlet with an AD user that has owner permission on the target storage account. [Our troubleshooting document](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#self-diagnostics-steps) provides more details on the checks we perform and their detailed explanation.

    $ResourceGroupName = "<resource-group-name-here>"
    $StorageAccountName = "<storage-account-name-here>"

    Debug-AzStorageAccountAuth -StorageAccountName $StorageAccountName -ResourceGroupName $ResourceGroupName -Verbose

Please continue further with this troubleshooter based on the result of this cmdlet.
