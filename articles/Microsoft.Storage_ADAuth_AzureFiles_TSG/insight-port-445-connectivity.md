<properties
    pageTitle="Unable to mount - Outbound Port 445 is blocked"
    description="Unable to mount - Outbound Port 445 is blocked"
    infoBubbleText="Unable to mount - Outbound Port 445 is blocked"
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
    articleId="052c98b8-980b-45f8-ab07-0348a7174616"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# Unable to mount - Outbound Port 445 is blocked
<!--issueDescription-->
In order for AD Auth to work properly, please make sure customer's client machine has outbound port 445 open for communication with Azure File Storage.
<!--/issueDescription-->

## **Recommended Steps**

1. Please ask the customer to review the solutions specified in this [public document](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#solution-for-cause-1-1). Possible solutions include unblocking 445 port with the help of their ISP/IT Admin or setting up a VPN. 
2. Once they have successfully opened the port or have setup the VPN, re-run the "Debug-AzStorageAccountAuth" cmdlet to make sure all the other checks pass successfully. If they do not, go back to previous step to further troubleshoot. 
3. If "Debug-AzStorageAccountAuth" completes successfully, ask the customer to try mounting the file share. If mount still fails, escalate.