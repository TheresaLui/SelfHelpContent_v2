<properties
pageTitle="Storage Account was throttled due to a scalability limit being exceeded"
description="Storage Account was throttled due to a scalability limit being exceeded"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="shines"
displayOrder=""
articleId="Storagev2insights_ingress_egress_IOPS_throttling"
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

Limit type: **<!--$LimitType--> LimitType <!--/$LimitType-->**<br><br>

We recommended that you configure Storage Analytics to monitor throttling on your Storage Account. This will enable you to monitor your application's increase in transaction volume to prevent or mitigate similar issues in the future. For further information, please see [monitoring, diagnostics and troubleshooting guide for Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting#metrics-show-an-increase-in-PercentThrottlingError).
<!--/issueDescription-->
