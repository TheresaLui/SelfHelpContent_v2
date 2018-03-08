<properties
pageTitle="Storage ingress egress IOPS overlimit"
description="Storage ingress egress IOPS overlimit"
service="microsoft.storage"
resource="storage"
authors="shines"
displayOrder=""
articleId="Storagev2insights_ingress_egress_IOPS_overlimit"
diagnosticScenario="Storage ingress egress IOPS overlimit"
selfHelpType="diagnostics"
supportTopicIds="32602726,32602727,32602761,32602762,32602885"
resourceTags="storage"
productPesIds="16459"
cloudEnvironments="public"
/>

# **Storage ingress egress IOPS overlimit RCA**
<!--issueDescription-->

Microsoft Azure team has concluded investigation of performance issue while accessing **<!--$AccountName-->Storage Account<!--/$AccountName-->**. The performance issue was due to storage scalability limits being reached.<br>
The storage account **<!--$AccountName-->Storage Account<!--/$AccountName-->** reached the following limits between **<!--$StartTime--> StartTime <!--/$StartTime-->** and **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**:.<br>

Limit type: **<!--$LimitType--> LimitType <!--/$LimitType-->**<br>
Limit imposed: <UPDATE THE LIMIT IMPOSED>[US regions: 20 Gbps for RA-GRS/GRS/ZRS, 30 Gbps for LRS | non-US regions: 10 Gbps for RA-GRS/GRS/ZRS, 15 Gbps     for LRS | custom quota value]<UPDATE THE LIMIT IMPOSED><br>

It is recommended to configure Storage Analytics to monitor throttling on the Storage Accounts. It will enable you to diagnose whether your application is generating transient increase in transaction volume or a permanent increase; and mitigate such issues pro-actively. For further information, please see monitoring, diagnostics and troubleshooting guide for Azure Storage..<br>
Regards,.<br>
Microsoft Azure Team

<!--/issueDescription-->