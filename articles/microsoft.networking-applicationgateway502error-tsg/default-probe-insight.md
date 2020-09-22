<properties
pageTitle="Application Gateway 502 Error: Default Probe Insight"
description="Application Gateway 502 Error: Default Probe Insight"
infoBubbleText= "Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="applicationGateway"
authors="JRMayberry"
ms.author="rimayber"
displayOrder=""
articleId="1df2874c-4674-4583-b091-11c49fb8dfeb"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec" 	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Application Gateway 502 Error: Default Probe Insight

<!--issueDescription-->
Server is not accessible or not giving a healthy response for the default probe. Directly access the server using the format <protocol>//127.0.0.1:<port>/ and check the response if it is in the acceptable range. Otherwise, create a custom probe with the appropriate hostname and path and associate it to the corresponding HTTP settings.
<!--/issueDescription-->
