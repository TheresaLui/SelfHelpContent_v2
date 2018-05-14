<properties
pageTitle="Classic Image attached message"
description="Classic Image attached message"
infoBubbleText="Classic Image attached message"
service="microsoft.storage"
resource="storage"
authors="passaree"
displayOrder=""
articleId="Storagev2insights_DeletionClassic_ImageAttached"
diagnosticScenario="Classic Image attached message"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="public"
/>

# **Classic Image has been detected**
<!--issueDescription-->
Microsoft Azure identified one or more active image(s) associated with <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**. All image(s) listed below must be deleted before deleting the <!--$ResourceType-->[ResourceType]<!--/$ResourceType-->: <br>

<!--$ImageList-->[ImageList]<!--/$ImageList-->

To delete a VM image: <br>

1. Sign into [Azure Portal](https://portal.azure.com) <br>
2. Search for "**VM images** (classic)" service and browse to it. <br>
3. Browse to an image listed above and delete it. <br>

Regards,<br>
Microsoft Azure Team
<!--/issueDescription-->
