<properties
pageTitle="Static Website integration with Azure Active Directory"
description="Static Website integration with Azure Active Directory"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="annayak"
ms.author="annayak"
displayOrder=""
articleId="storagev2insights_blob_staticwebsite_azuread_integration"
diagnosticScenario="Static Website integration with Azure Active Directory"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest"
/>

# Does Static Website support Azure AD?

<!--issueDescription-->
No Static Website currently doesn't support Azure AD authentication.
<!--/issueDescription-->

## **Recommended Steps**

Currently Static Website doesn't support **[Azure AD](https://docs.microsoft.com/azure/storage/common/storage-auth-aad)** authentication even though the blob endpoint does. The web endpoint could be publically accessed by anonymously by anyone connected to the internet.</br>Static website also doesn't support use of social IDPs like Google Auth or Facebook using OpenID Connect.
