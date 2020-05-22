<properties
pageTitle="Application Gateway 502 Error: Backend Server Certificate needs to be whitelisted Insight"
description="Application Gateway 502 Error: Backend Server Certificate needs to be whitelisted Insight"
infoBubbleText= "Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="applicationGateway"
authors="JRMayberry"
ms.author="rimayber"
displayOrder=""
articleId="5b90a2c2-d59e-4691-a198-b3f8db6b2a8e"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec" 	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Application Gateway 502 Error: Backend Server Certificate needs to be whitelisted Insight

<!--issueDescription-->
Certificate uploaded in Application Gateway does not match with the certificate used by the backend server or the certificate might be invalid. To resolve this, check the certificate returned by the server when accessed directly and if there is a mismatch, upload it to the Application Gateway’s respective HTTP Settings.
<!--/issueDescription-->
