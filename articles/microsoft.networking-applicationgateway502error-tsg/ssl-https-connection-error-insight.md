<properties
pageTitle="Application Gateway 502 Error: Https probe connection error Insight"
description="Application Gateway 502 Error: Https probe connection error Insight"
infoBubbleText= "Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="applicationGateway"
authors="JRMayberry"
ms.author="rimayber"
displayOrder=""
articleId="b47b164d-ea9b-494c-9ee4-340d1a1db0b8"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec" 	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Application Gateway 502 Error: Https probe connection error Insight

<!--issueDescription-->
Application Gateway failed to establish a successful TLS handshake with the backend server. To resolve this, check the SSL Policy configured on the Application Gateway and if the backend supports it (minimum TLS version supported, Cipher Suites used for the SSL communication). If there is a policy mismatch, configure the right SSL policy on the Application Gateway or the backend server so that they match.
<!--/issueDescription-->
