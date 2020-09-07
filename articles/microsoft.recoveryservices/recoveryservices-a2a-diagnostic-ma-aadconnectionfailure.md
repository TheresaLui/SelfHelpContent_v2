<properties
	pageTitle="Mobility service Configuration failed due to AAD connectivity issue"
	description="Mobility service Configuration failed due to AAD connectivity issue"
	infoBubbleText="Some suggestions have been found to help solve your issue. Please see details on the right."
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="genlin"
	ms.author="asgang"
	displayOrder=""
	articleId="AADConnectionFailure"
	diagnosticScenario="ASRA2AMobilityAgentConfiguratorFailure"
	selfHelpType="Diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Mobility service Configuration failed due to AAD connectivity issue
<!--issueDescription-->
Failed to configure Mobility service with error **A2AMobilityServiceConfiguratorConfigurationFailed**. The connection to Azure Active Directory (AAD) cannot be established while using proxy. This issue occurs if the custom proxy settings are invalid or Azure Site Recovery Mobility service fail to detect the proxy settings.
<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue, follow these steps:

1. Make sure that the proxy settings from Internet Explorer on Windows or **/etc/environment** on Linux are correct
2. If the error still occurs, set proxy only for the Site Recovery Mobility service. To do this, you can provide the proxy details in ProxyInfo.conf that is located at **/usr/local/InMage/config/** for Linux VM, or **C:\ProgramData\Microsoft Azure Site Recovery\Config** for Windows VM.
3. The ProxyInfo.conf should have the proxy settings in the following INI format. The Mobility service supports only un-authenticated proxies:

```
[proxy]
Address=http://1.2.3.4
Port=567
```	
