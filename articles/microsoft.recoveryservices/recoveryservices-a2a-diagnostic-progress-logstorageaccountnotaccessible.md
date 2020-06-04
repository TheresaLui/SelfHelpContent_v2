<properties
    pageTitle="Replication is not progressing as log storage is not accessible"
    description="Replication status is critical because the log storage account in Azure is not accessible from Source Machine."
    infoBubbleText="Site recovery Mobility Service on the source virtual machine is not able to access to the cache storage account. Please see details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="genlin"
    ms.author="asgang,genli"
    displayOrder=""
    articleId="ASR_A2A_ReplicationNotProgressing_LogStorageAccountNotAccessible"
    diagnosticScenario="ASRA2AReplicationNotProgressingHealthIssues"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Replication is not progressing as log storage is not accessible

<!--issueDescription-->
Replication status is critical because Azure Site Recovery(ASR) Mobility Service on Source Machine is not able to access the log storage account in Azure.
<!--/issueDescription-->

## **Recommended Steps**

Verify the log storage in Azure is accessible from Source Machine. To do that, follow these steps:

1. Login to Source Machine with administrator privileges on Windows OS or as user root on Linux OS
2. Check if the log storage account is accessible by using tools like [Azure Storage Explorer](https://azure.microsoft.com/features/storage-explorer/) and the network latencies in uploading the data is good
3. Work with the network team to resolve any network issues
4. On the Source Machine, check the following log for any errors:

    - **Windows**: C:\\Program Files (x86)\\Microsoft Azure Site Recovery\\agent\\svagents*log
    - **Linux**: /var/log/svagents*log
