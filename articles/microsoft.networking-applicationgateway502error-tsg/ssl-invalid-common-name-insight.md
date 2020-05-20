<properties
pageTitle="Application Gateway 502 Error: Backend Server Certificate Invalid Common Name Insight"
description="Application Gateway 502 Error: Backend Server Certificate Invalid Common Name Insight"
infoBubbleText= "Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="applicationGateway"
authors="JRMayberry"
ms.author="rimayber"
displayOrder=""
articleId="e5e2bd69-9588-41de-b7c0-026464dc3f19"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec" 	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Application Gateway 502 Error: Backend Server Certificate Invalid Common Name Insight

<!--issueDescription-->
Application Gateway validates if the Hostname specified in the backend http setting matches that of the Common Name (CN) presented by the backend server’s SSL certificate. If you see the above-mentioned error message, it means that the Common Name (CN) of the backend certificate does not match the hostname configured in the custom probe or the HTTP Settings (in case “Pick Hostname from Backend HTTP Settings” is chosen). If you are using a default probe, the hostname would be set as “127.0.0.1”. If that’s not a desired value, you should create a custom probe and associate it to the HTTP Settings.
<!--/issueDescription-->
