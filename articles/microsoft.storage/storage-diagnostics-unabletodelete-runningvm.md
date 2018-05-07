<properties
pageTitle="Running VM attached message"
description="Running VM attached message"
infoBubbleText="Running VM has been detected."
service="microsoft.storage"
resource="storage"
authors="passaree"
displayOrder=""
articleId="Storagev2insights_DeletionARM_RunningVM"
diagnosticScenario="Running VM attached"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="public"
/>

# **Running VM has been detected**

<!--issueDescription-->
Microsoft Azure identified one or more virtual machine(s) that are actively using disk(s) hosted in the <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**. The following actions must be completed for all disk(s) listed below before deleting the <!--$ResourceType-->[ResourceType]<!--/$ResourceType-->: 

1. <strong>OS Disk</strong> - stop and delete the virtual machine <br>
2. <strong>Data Disk</strong> - detach the disk from the virtual machine <br>

All impacted virtual machine(s) and its corresponding disk(s) are below: <br>

<!--$ResourceList-->[ResourceList]<!--/$ResourceList-->

For more information on troubleshooting this issue, see [troubleshoot storage resource deletion errors.](https://docs.microsoft.com/azure/virtual-machines/windows/storage-resource-deletion-errors)<br>

Regards,<br>
Microsoft Azure Team
<!--/issueDescription-->