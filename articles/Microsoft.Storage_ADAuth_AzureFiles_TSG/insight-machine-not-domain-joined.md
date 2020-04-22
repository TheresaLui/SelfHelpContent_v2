<properties
    pageTitle="Unable to mount - Client machine is not joined to On-Prem AD"
    description="Unable to mount - Client machine is not joined to On-Prem AD"
    infoBubbleText="Unable to mount - Client machine is not joined to On-Prem AD"
    service="microsoft.storage"
    resource="storageAccounts"
    authors="yagohel23"
    ms.author="yagohel"
    displayOrder=""
    selfHelpType="Diagnostics"
    supportTopicIds="32689882"
    resourceTags=""
    productPesIds="1003478"
    cloudEnvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
    articleId="695c40fc-6fdd-48ec-a94b-615ab18bd857"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# Unable to mount - Client machine is not joined to On-Prem AD
<!--issueDescription-->
In order for AD Auth to work properly, please make sure customer's client machine is doamin-joined to On-Prem AD.
<!--/issueDescription-->

## **Recommended Steps**

1. Please ask the customer to domain-join their client machine. This is one of the prerequisites as defined [here](https://docs.microsoft.com/azure/storage/files/storage-files-identity-auth-active-directory-enable#prerequisites). 
2. Once they have successfully domain-joined the machine, re-run the "Debug-AzStorageAccountAuth" cmdlet to make sure all the other checks pass successfully. If they do not, go back to previous step to further troubleshoot. 
3. If "Debug-AzStorageAccountAuth" completes successfully, ask the customer to try mounting the file share. If mount still fails, escalate.