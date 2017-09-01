<properties
pageTitle="Running VM attached message"
description="Running VM attached message"
infoBubbleText="Running VM has been detected."
service="microsoft.storage"
resource="storage"
authors="divka78, passaree"
displayOrder=""
articleId="StorageDeletionARM_RunningVM"
diagnosticScenario="Running VM attached"
selfHelpType="diagnostics"
supportTopicIds="32551656"
resourceTags="windows"
productPesIds="15629"
cloudEnvironments="public"
/>

# **Running VM has been detected**

<!--issueDescription-->
Microsoft Azure identified one or more virtual machines that are actively using disks hosted in the storage account <!--$StorageAccountName-->[StorageAccountName]<!--/$StorageAccountName-->. The following actions must be completed for all disk(s) listed below before deleting the storage account: 

1. <strong>OS Disk:</strong> stop and deleted the virtual machine
2. <strong>Data Disk:</strong> detach the disk from the virtual machine

Here is the list of all impacted virtual machines and the corresponding disks:
<ol>
<li><strong>VM Name:</strong> <!--$VMName1-->[VMName1]<!--/$VMName1-->; <strong>OS Disk:</strong> <!--$OSDisk1-->[OSDisk1]<!--/$OSDisk1-->; <strong>Data Disk(s):</strong> <!--$DataDisk1_1-->[DataDisk1_1]<!--/$DataDisk1_1-->, <!--$DataDisk1_2-->[DataDisk1_2]<!--/$DataDisk1_2--> </li>
<li><strong>VM Name:</strong> <!--$VMName2-->[VMName2]<!--/$VMName2-->; <strong>OS Disk:</strong> <!--$OSDisk2-->[OSDisk2]<!--/$OSDisk2--> </li>
<li><strong>VM Name:</strong> <!--$VMName3-->[VMName3]<!--/$VMName3-->; <strong>Data Disk(s):</strong> <!--$DataDisk3_1-->[DataDisk3_1]<!--/$DataDisk3_1--></li>
</ol>
<!--/issueDescription-->

