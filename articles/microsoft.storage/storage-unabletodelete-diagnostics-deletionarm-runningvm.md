<properties
pageTitle="Running VM attached message"
description="Running VM attached message"
infoBubbleText="A running VM is attached to the disk. See details on the right."
service="microsoft.storage"
resource="storage"
authors="divka78, passaree"
displayOrder=""
articleId="StorageDeletionARM_RunningVM"
diagnosticScenario="Running VM attached"
selfHelpType="diagnostics"
supportTopicIds="32602694"
resourceTags="windows"
productPesIds="15629"
cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# **Running VM has been detected**

<!--issueDescription-->
Microsoft Azure identified one or more virtual machines that are actively using disks hosted in the storage account <!--$StorageAccountName-->[StorageAccountName]<!--/$StorageAccountName-->. The following actions must be completed for all disk(s) listed below before deleting the storage account: 

1. <strong>OS Disk:</strong> stop and deleted the virtual machine
2. <strong>Data Disk:</strong> detach the disk from the virtual machine

Here is the list of all impacted virtual machines and the corresponding disks:

<!--$ResourceList-->[ResourceList]<!--/$ResourceList-->

<!--/issueDescription-->

