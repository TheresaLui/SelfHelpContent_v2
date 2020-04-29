<properties
pageTitle="Application Gateway 502 Error: Custom Probe Insight"
description="Application Gateway 502 Error: Custom Probe Insight"
infoBubbleText= "Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="applicationGateway"
authors="JRMayberry"
ms.author="rimayber"
displayOrder=""
articleId="b6df889e-aaf1-470f-9c7a-421027699331"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec" 	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Application Gateway 502 Error: Custom Probe Insight

<!--issueDescription-->
Server response does not match the custom probe configuration. Access the server directly with the settings mentioned in the custom probe and edit the hostname, path and match parameters to appropriate values.

For example, if probe path is configured as "/path/" and if there is no directory in the server called "path", the probe will fail as the server returns a 404 Page Not Found error. In that case, edit the path to the right value where the server can return a healthy response.
<!--/issueDescription-->
