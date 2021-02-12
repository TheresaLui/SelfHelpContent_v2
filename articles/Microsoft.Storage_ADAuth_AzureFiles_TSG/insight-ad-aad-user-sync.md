<properties
    pageTitle="Unable to mount - Logged on AD user is not synced to Azure AD"
    description="Unable to mount - Logged on AD user is not synced to Azure AD"
    infoBubbleText="Unable to mount - Logged on AD user is not synced to Azure AD"
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
    articleId="a5e2f35b-a256-44a4-84c3-8305ca723c62"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# Unable to mount - Logged on AD user is not synced to Azure AD
<!--issueDescription-->
In order for AD Auth to work properly, logged on AD user's identity must be synced to Azure AD.
<!--/issueDescription-->

## **Recommended Steps**

1. You can verify if the AD User's identity is synced to Azure AD by using [this TSG](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/295529/ADAuth-for-Azure-Files-AAD-Sync-Verify-if-the-on-prem-AD-user-is-synced-to-AAD). If you don't see the identity synced with AAD, please engage the AAD team to verify customer's AAD Sync setup and take their help to resolve this sync issue. Use this support topic path to cut a collaboration task with them: "Azure/Azure Active Directory User Provisioning and Synchronization/Syncing from AD to AAD". 
2. Once AAD sync issue is resolved, re-run the "Debug-AzStorageAccountAuth" cmdlet to make sure all the other checks pass successfully. If they do not, go back to previous step to further troubleshoot. 
3. If "Debug-AzStorageAccountAuth" completes successfully, ask the customer to try mounting the file share. If mount still fails, escalate.
