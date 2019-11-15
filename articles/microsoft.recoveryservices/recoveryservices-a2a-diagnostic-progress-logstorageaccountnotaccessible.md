<properties
    pageTitle="Fail to access the cache storage account"
    description="Fail to access the cache storage account"
    infoBubbleText="Site recovery Mobility Service on the source virtual machine is not able to access to the cache storage account. Please see details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="genlin"
    ms.author="asgang,genli"
    displayOrder=""
    articleId="ASR_A2A_ReplicationNotProgressing_LogStorageAccountNotAccessible"
    diagnosticScenario="ASRV2AReplicationNotProgressingHealthIssues"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public"
/>

# Fail to access the cache storage account
<!--issueDescription-->
Replication status is critical. This issue is caused by the Site recovery Mobility Service on the source virtual machine is not able to access to the cache storage account to replicate data.
<!--/issueDescription-->

## **Recommended Steps**

Follow these steps to check if the virtual machine can access the cache storage account:

1. Login to source virtual machine by using administrator privileges on Windows OS or as user root on Linux OS
2. Check if the cache storage account is accessible by using tools like [Azure Storage Explorer](https://azure.microsoft.com/features/storage-explorer/)
3. Check if there is a hight network latency when you upload the data from the source virtual machine
