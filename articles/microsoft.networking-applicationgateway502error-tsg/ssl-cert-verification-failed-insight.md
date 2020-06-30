<properties
pageTitle="Application Gateway 502 Error: Certificate Verification Failed Insight"
description="Application Gateway 502 Error: Certificate Verification Failed Insight"
infoBubbleText= "Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="applicationGateway"
authors="JRMayberry"
ms.author="rimayber"
displayOrder=""
articleId="48fe682d-6147-4e15-9f8d-336079f5d944"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec" 	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Application Gateway 502 Error: Certificate Verification Failed Insight

<!--issueDescription-->
Application Gateway verifies the validity of the backend server certificate. If it couldn’t verify the validity due to some issue, it considers the server as Unhealthy. To resolve this issue, check the certificate on your server if it is properly created. 
For example, you can use OpenSSL to verify the certificate and its properties and try reuploading the certificate to the Application Gateway's HTTP settings.
<!--/issueDescription-->
