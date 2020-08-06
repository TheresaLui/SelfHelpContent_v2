<properties
pageTitle="Clientside Latency"
description="Clientside Latency"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="shines"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_Clientside_Latency"
diagnosticScenario="Clientside Latency"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# **Clientside Latency RCA**
<!--issueDescription-->

Microsoft Azure team has concluded the investigation of performance issue while accessing **<!--$AccountName-->Storage account<!--/$AccountName-->** on **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)**. Your application is experiencing high end to end latency due to resource contention on client side.<br>

The Azure Storage service side latency was **<!--$ServerLatency--> average server latency <!--/$ServerLatency-->** but client perceived latency spiked to **<!--$ClientLatency--> client latency <!--/$ClientLatency-->** at or around **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)**.<br>
Please refer to Performance Analysis and Troubleshooting guide on the client application to further investigate and mitigate the issue.<br>

Regards,<br>
Microsoft Azure Team
<!--/issueDescription-->