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
Microsoft Azure identified one or more active image(s) hosted in the <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**. Please ensure all image(s) listed below are removed before deleting the <!--$ResourceType-->[ResourceType]<!--/$ResourceType-->: 

<!--$ImageList-->[ImageList]<!--/$ImageList-->

VM image(s) can be delete by: <br>
1. Sign into [Azure Portal](https://portal.azure.com) <br>
2. Search for "**VM images** (classic)" service and browse to it. <br>
3. Find Storage Account that you wish to delete in the "STORAGE ACCOUNT" tab. <br>
4. For all VM image(s) in the Storage Account, select each image and delete it. 

[Note] Alternatively, if you attempt to delete the Storage Account directly from the Portal, it will list all images that is blocking deletion on the Storage Account. <br>

Regards,<br>
Microsoft Azure Team
<!--/issueDescription-->
