<properties
pageTitle="Net use 1326 error - Computer Accounts not supported Insight"
description="Net use 1326 error - Computer Accounts not supported Insight"
infoBubbleText= "We detected that the customer is trying to access file share using a computer account."
service="microsoft.storage"
resource="storageAccounts"
authors="yagohel23"
ms.author="yagohel"
displayOrder=""
articleId="85756996-b184-46e6-8865-c7e0fa88d64c"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds="32689882"
resourceTags=""
productPesIds="1003478"
cloudEnvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Net use 1326 error - Computer Accounts not supported Insight
<!--issueDescription-->
There's no support for access to Azure Files via a computer identity.  Customer needs to adjust application to use a user identity that is synced to AAD.

Sample customer communication

Hi customer, we don't have a plan to extend support to Computer Accounts in Preview. The reason is that Computer Accounts are not supported identities for RBAC based access control management used for share level permission assignment. For now, the recommendation is to use service logon accounts instead of computer accounts. We are evaluating options to address this gap in future releases.
<!--/issueDescription-->