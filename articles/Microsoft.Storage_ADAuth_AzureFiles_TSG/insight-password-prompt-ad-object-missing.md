<properties
    pageTitle="User gets prompted for credentials while running net use command - computer account missing"
    description="User gets prompted for credentials while running net use command - computer account missing"
    infoBubbleText="User gets prompted for credentials while running net use command - computer account missing"
    service="microsoft.storage"
    resource="storageAccounts"
    authors="yagohel23"
    ms.author="yagohel"
    displayOrder=""
    selfHelpType="Diagnostics"
    supportTopicIds="32689882"
    resourceTags=""
    productPesIds="1003478"
    cloudEnvironments="public"
    articleId="7af24444-f9b2-4980-9988-cffc93fa3ccf"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# User gets prompted for credentials while running net use command - computer account missing
<!--issueDescription-->
Please run the following PowerShell command to validate if the object exists - Get-AzStorageAccountADObject -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"

If the object doesnt exist, please work with the customer and recreate the AD Object using PowerShell. 

If the object does exist, collect a wireshark trace while reproducing the issue and further escalate this issue. 
<!--/issueDescription-->