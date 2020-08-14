<properties
pageTitle="Customer-managed account failover feature is currently unavailable"
description="Customer-managed account failover feature is currently unavailable"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="AngshumanNayakMSFT"
ms.author="annayak"
displayOrder=""
articleId="storage_acctfailover_currrently_blocked_by_PG_ICM193261113.md"
diagnosticScenario="Customer-managed account failover feature is currently unavailable"
selfHelpType="diagnostics"
supportTopicIds="32631234"
resourceTags="storage"
productPesIds="15629"
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# Customer-managed account failover feature is currently unavailable
<!--issueDescription--> ‏‏‎
 <!--/issueDescription-->
## **We found an issue - Customer-managed account failover feature is currently unavailable**

Customer-managed account failover feature is currently unavailable due to a service issue that impacts access to the storage account after failover. We are working with priority to address the issue, validate and deploy the fix. We apologize for the inconvenience this has caused.

## **Recommended Steps**

If you have an immediate need to perform account failover for disaster recovery of your production workload, please submit a support ticket with details on your failover scenario. We will work with you to perform the failover from the service backend. For all other non-critical scenarios, we recommend waiting for the customer-managed failover feature to be enabled again.

More information on the customer managed storage account failover can be found here;[Storage Disaster Recovery Guidance](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance)

Alternatively you can backup your data to a second storage account in your target region by performing another write operation. [Copying data as an alternative to failover](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance#copying-data-as-an-alternative-to-failover)

Once the fix is deployed the failover option be made available again. You can use either of the following to ascertain that the issue is resolved.

1. Failover of an account works
2. This diagnostic doesn't show up anymore when trying to submit a case