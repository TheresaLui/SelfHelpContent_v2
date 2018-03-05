<properties
pageTitle="Storage ingress egress IOPS overlimit"
description="Storage ingress egress IOPS overlimit"
infoBubbleText="An active lease has been detected"
service="microsoft.storage"
resource="storage"
authors="shines"
displayOrder=""
articleId="storagedeletionarm-existinglease"
diagnosticScenario="Storage ingress egress IOPS overlimit"
selfHelpType="diagnostics"
supportTopicIds="32602694"
resourceTags="windows"
productPesIds="15629"
cloudEnvironments="public"
/>

# **Storage ingress egress IOPS overlimit RCA**
<!--issueDescription-->

Incident Information
 
Incident ID	<SR Id>

Incident Title	<SR Title>

Service(s) Impacted	<Blob, File, Table or Queue>

Microsoft Azure team has concluded investigation of performance issue while accessing <Storage Account name> on <DateTime>. The performance issue was due to storage scalability limits being reached.
The storage account <Storage Account name> reached the following limits between <StartDateTime> and <EndDateTime>:
 
<CHOOSE THE LIMIT TYPE>
  
  Limit type: [IOPS, Ingress, Egress]
  
<UPDATE THE LIMIT IMPOSED>
  
  Egress limit imposed: [US regions: 20 Gbps for RA-GRS/GRS/ZRS, 30 Gbps for LRS | non-US regions: 10 Gbps for RA-GRS/GRS/ZRS, 15 Gbps     for LRS | custom quota value]
  
<UPDATE THE REQS ABOVE LIMIT>
  
  Egress above limit:

It is recommended to configure Storage Analytics to monitor throttling on the Storage Accounts. It will enable you to diagnose whether your application is generating transient increase in transaction volume or a permanent increase; and mitigate such issues pro-actively. For further information, please see monitoring, diagnostics and troubleshooting guide for Azure Storage.

Regards,

Microsoft Azure Team

<!--/issueDescription-->
