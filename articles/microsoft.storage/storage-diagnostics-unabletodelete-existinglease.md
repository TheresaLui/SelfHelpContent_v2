<properties
pageTitle="ARM lease exist"
description="ARM lease exist"
infoBubbleText="An active lease has been detected"
service="microsoft.storage"
resource="storage"
authors="passaree"
displayOrder=""
articleId="Storagev2insights_all_DeletionARM_Lease"
diagnosticScenario="An active non page blob lease has been detected"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="public"
/>

# **An active lease has been detected**

<!--issueDescription-->
Microsoft Azure identified one or more active lease(s) associated with <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**. All lease(s) listed below must be broken before deleting the <!--$ResourceType-->[ResourceType]<!--/$ResourceType-->: <br>

<!--$LeaseList-->[LeaseList]<!--/$LeaseList-->
<br>

To break a lease: <br>
1. Sign into [Azure Portal](https://portal.azure.com) <br>
2. Browse to each leased resource listed above and break its lease.<br>
3. Retry delete operation after all leased object(s) listed above are broken. <br>

Regards,<br>
Microsoft Azure Team
<!--/issueDescription-->
