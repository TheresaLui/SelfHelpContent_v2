<properties
pageTitle="Storage IOPS overlimit"
description="Storage IOPS overlimit"
service="microsoft.storage"
resource="storage"
authors="shines"
displayOrder=""
articleId="Storagev2insights_ingress_egress_IOPS_overlimit"
diagnosticScenario="Storage IOPS overlimit"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="storage"
productPesIds=""
cloudEnvironments="public"
/>

# Storage Account **<!--$AccountName-->[AccountName]<!--/$AccountName-->** was throttled due to a scalability limit being exceeded
<!--issueDescription-->
The Storage Account **<!--$AccountName-->[AccountName]<!--/$AccountName-->** exceeded its [storage scalability limits](https://azure.microsoft.com/documentation/articles/storage-scalability-targets/). This can result in storage operation failures and increased latency.<br>

The following limits were reached between **<!--$StartTime--> StartTime <!--/$StartTime-->** and **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**:<br>

Limit type: **<!--$LimitType--> LimitType <!--/$LimitType-->**<br>
Limit imposed: <UPDATE THE LIMIT IMPOSED>[US regions: 20 Gbps for RA-GRS/GRS/ZRS, 30 Gbps for LRS | non-US regions: 10 Gbps for RA-GRS/GRS/ZRS, 15 Gbps     for LRS | custom quota value]<UPDATE THE LIMIT IMPOSED><br>

We recommended that you configure Storage Analytics to monitor throttling on your Storage Accounts. This will enable you to monitor your application's increase in transaction volume to prevent or mitigate similar issues in the future. For further information, please see [monitoring, diagnostics and troubleshooting guide for Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting).<br>
<!--/issueDescription-->
