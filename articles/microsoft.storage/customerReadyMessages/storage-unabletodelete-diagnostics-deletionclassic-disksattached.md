<properties
pageTitle="Classic Disk attached message"
description="Classic Disk attached message"
infoBubbleText="Classic Disk attached message"
service="microsoft.storage"
resource="storage"
authors="passaree"
displayOrder=""
articleId="Storagev2insights_DeletionClassic_RunningVM"
diagnosticScenario="Running VM attached"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="public"
/>

# **Classic VM has been detected**

<!--issueDescription-->
Microsoft Azure identified one or more classic virtual machines that are actively using disks hosted in the <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**. The following actions must be completed for all disk(s) listed below before deleting the <!--$ResourceType-->[ResourceType]<!--/$ResourceType-->: 

1. <strong>OS Disk:</strong> stop and deleted the virtual machine
2. <strong>Data Disk:</strong> detach the disk from the virtual machine

Here is the list of all impacted virtual machines and the corresponding disks:

<!--$ResourceList-->[ResourceList]<!--/$ResourceList-->
<br>

Regards,<br>
Microsoft Azure Team
<!--/issueDescription-->
