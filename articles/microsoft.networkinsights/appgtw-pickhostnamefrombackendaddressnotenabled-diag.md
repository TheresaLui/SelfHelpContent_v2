<properties
pageTitle="Application Gateway Pick Host Name Not Set"
description="Application Gateway Pick Host Name Not Set"
infoBubbleText="Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="ApplicationGateway"
authors="chadmath"
displayOrder="10"
articleId="ApplicationGatewaypickhostnamemissing"
diagnosticScenario="ApplicationGatewaypickhostnamemissing"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureApplicationGateway"
/>
# Application Gateway Pick Host Name Not Set
<!--issueDescription-->
**'PickHostNameFromBackendAddress'** is not enabled on this Application Gateway. If the backend is a multi-tenant resource, such as, Azure Web Apps or App Service Environments, PickHostNameFromBackendAddress might need to be enabled if backend FQDN does not match with the host sent in the URL.
<!--/issueDescription-->
## More Information
Check the following resources to validate if the PickHostNameFromBackendAddress setting is required.

* [Application Gateway with an App Service](https://blogs.msdn.microsoft.com/waws/2017/11/21/setting-up-application-gateway-with-an-app-service-that-uses-azure-active-directory-authentication/)
* [Configure App Service Web Apps with Application Gateway](https://docs.microsoft.com/azure/application-gateway/application-gateway-web-app-powershell)
