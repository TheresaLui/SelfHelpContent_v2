<properties
	pageTitle="Database Connectivity issue due to frozen VM detected"
	description="IsFrozenVM"
	infoBubbleText="Found recent connectivity issue. See details on the right."
	service="microsoft.sql"
	resource="servers"
	authors="subbu-kandhaswamy"
	ms.author="subbuk"
	displayOrder=""
	articleId="IsFrozenVm_A4F4CB4A-E3C6-4001-B3D3-278FD7FC70EA"
	diagnosticScenario="SqlLts"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Connection attempts to your database **<!--$DatabaseName--> DatabaseName <!--/$DatabaseName-->** have recently failed from <!--$StartFreezeTime--> StartFreezeTime <!--/$StartFreezeTime--> UTC to <!--$EndFreezeTime--> EndFreezeTime <!--/$EndFreezeTime--> UTC due to a frozen VM issue. As soon as the problem was detected, automatic recovery actions were started and the database was returned to a stable state. If your database is still unavailable, please create a support ticket.
<!--/issueDescription-->

**Summary of Impact**

Azure Virtual Machines powers our IaaS and PaaS offerings, including SQL DB and Cosmos DB. We have detected two issues that degrade the availability of VMs:

  * Unexpected reboots
  * Read/write operations appeared frozen and I/O had come to a crawl

These issues impacted a small percentage of customers (approximately .01% a day). However, that number has recently increased to approximately 0.1% a day.

When a VM supporting SQL DB or Cosmos DB gets into this state, databases with primary replicas on that VM become unavailable. If the VM reboots, Azure Service Fabric identifies a new replica as primary, which results in the database being unavailable for only a short period. However, if the IO operations on the VM are frozen, this failover does not occur. In that case, impacted databases remain unavailable for an extended period of time.

There is a high priority Investigation into why VMs are getting into this state. Teams are working around the clock to identify mitigations to prevent impact to customer databases, find the root cause, and apply remediations so this issue no longer occurs.

**Root Cause Investigation**

Information from the VMs in this state and telemetry from the VMs when they reboot or suffer I/O freeze is being analyzed. So far, Azure believes the degradation started after a Host OS update. When the update occurred, Azure did not have telemetry in place to catch the VMs before getting into this state. Azure has deployed a fix to reduce the occurrence of the problem.

Engineers continue to analyze telemetry, host dumps, and logs to identify the root cause. Azure expects this will shortly lead to fixes to completely eradicate the problem.

**Mitigation in Progress**

Specific mitigation steps are being taken while the root cause and a fix is identified:

1. A hardware level signal has been identified related to specific actions on the disk controller stack. These actions cause drives to be unavailable from some codepaths. Code is being deployed to detect this signal within seconds of occurrence and automatically restart frozen VMs. This signal is being refined to minimize false positives (currently about 25%). Once refined, the deployment will be rolled out progressively across Azure.
2. A signal to detect frozen operations, based on checking read/write operations on all disks at regular intervals is also being developed. This signal detects issues with a lower false positive rate (about 25%). However, the detection and automated mitigation takes 5 minutes. The system to detect the signal has been deployed worldwide to SQL DB VMs and is being refined.
3. Azure is developing a mechanism to identify frozen VMs through the loss of telemetry of a VM, or the VM entering an unresponsive state from perspective of the other VMs that communicate with it. This mechanism a low false positive rate (about 10%), and a low false negative rate (about 5%). However, detection and automatic mitigation takes 45 minutes. This system is deployed worldwide to SQL and Cosmos DB.
	
Azure is continuing to refine the above signals as more telemetry is analyzed.
