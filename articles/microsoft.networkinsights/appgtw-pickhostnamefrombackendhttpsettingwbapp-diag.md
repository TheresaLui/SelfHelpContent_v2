<properties
pageTitle="PickHostNameFromBackendHttpSettings Not Enabled For Azure Web App"
description="PickHostNameFromBackendHttpSettings Not Enabled For Azure Web App"
infoBubbleText="Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="ApplicationGateway"
authors="chadmath"
displayOrder="10"
articleId="AppGwPickHostNameFromBackendHttpSettingsNotEnabledForAzureWebAppInsight"
diagnosticScenario="AppGwPickHostNameFromBackendHttpSettingsNotEnabledForAzureWebAppInsight"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureApplicationGateway"
/>
# Application Gateway Diagnostic Result
<!--issueDescription-->
Microsoft Azure has identified the FQDN **<!--$Fqdn-->[Fqdn]<!--/$Fqdn-->** is an Azure Web App and PickHostNameFromBackendHttpSettings is not enabled for the Probe. The Host listed in Probe **<!--$ProbeHost-->[ProbeHost] <!--/$ProbeHost--> does not match the FQDN in the Backend. 
<!--/issueDescription-->
## **Steps to resolve the issue**
PickHostNameFromBackendHttpSettings must be enabled on the Health Probe when the Backend server is an Azure Web App, or the Host in the Health Probe must match the backend FQDN. Learn more [here](https://docs.microsoft.com/azure/application-gateway/application-gateway-web-app-powershell#configure-a-web-app-behind-an-existing-application-gateway) on how to correctly configure this setting.
