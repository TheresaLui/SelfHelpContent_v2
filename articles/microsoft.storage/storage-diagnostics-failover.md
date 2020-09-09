<properties
pageTitle="We found an issue with account failover"
description="We found an issue with account failover"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="sijia"
ms.author="siz"
displayOrder=""
articleId="Storagev2insights_AccountFailoverIssue"
diagnosticScenario="We found an issue with account failover"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# We found an issue with account failover
<!--issueDescription-->
Customer-managed account failover feature is currently unavailable due to a service bug that may impact access to the storage account after failover. We are working with priority to fix the problem, validate and deploy the fix. We apologize for the inconvenience this has caused.
<!--/issueDescription-->

## **Recommended Steps**

If you have an immediate need to perform account failover for disaster recovery of your production workload, please submit a support ticket with details on your failover scenario. We will work with you to perform the failover from the service backend. For all other non-critical scenarios, we recommend waiting for the customer-managed failover feature to be enabled again. Alternatively you can backup your data to a second storage account in your target region by performing another write operation.
