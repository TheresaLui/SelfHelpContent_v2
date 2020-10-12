<properties
pageTitle="Application Gateway 502 Error: Root Certificate Mismatch Insight"
description="Application Gateway 502 Error: Root Certificate Mismatch Insight"
infoBubbleText= "Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="applicationGateway"
authors="JRMayberry"
ms.author="rimayber"
displayOrder=""
articleId="9ad337fe-ad81-46a1-af42-fbfaccdf6660"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec" 	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Application Gateway 502 Error: Root Certificate Mismatch Insight

<!--issueDescription-->
The certificate that has been uploaded to the Application Gateway HTTP Settings must match with the root certificate of the backend server certificate and the entire chain of the backend certificate must be verified. To resolve this, if there is a mismatch, please extract the root certificate of the backend server certificate and upload it to the Application Gateway’s respective HTTP Settings.
<!--/issueDescription-->
