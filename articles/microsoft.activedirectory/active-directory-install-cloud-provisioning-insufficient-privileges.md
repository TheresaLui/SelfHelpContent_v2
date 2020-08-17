<properties
	pageTitle="Problem installing Cloud Provisioning Agent"
	description="Problem installing Cloud Provisioning agent due to insufficient privileges"
	infoBubbleText="Problem installing Cloud Provisioning agent"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	ms.author="Dhanyahk"
	displayOrder="2224"
	articleId="1957ed0c-6e3c-4f50-ab61-983341597856"
	diagnosticScenario=""
	selfHelpType="resource"
	supportTopicIds="32689667"
	resourceTags="cloud_provisioning"
	productPesIds="16666"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureIdentity_User"
/>

# Installation issues around Cloud Provisioning due to insufficient privileges

You are unable to install the Cloud Provisioning agent (Preview) and getting the error "Service 'Microsoft Azure AD Connect Provisioning Agent' failed to start. Verify that you have sufficient privileges to start the system services."

## **Recommended Steps**

This problem is typically caused by a group policy that prevented permissions from being applied to the local NT Service account created by the installer (NT SERVICE\AADConnectProvisioningAgent). These permissions are required to start the service.

1. Sign in to the server with an administrator account
2. Open Services by either navigating to it or by going to Start > Run > Services.msc
3. Under Services, double-click Microsoft Azure AD Connect Provisioning Agent
4. On the Log On tab, change this account to a domain admin, then restart the service

## **Recommended Documents**

* [Troubleshooting additional agent install issues](https://docs.microsoft.com/azure/active-directory/cloud-provisioning/how-to-troubleshoot#agent-problems)
* [Troubleshooting object synchronization issues](https://docs.microsoft.com/azure/active-directory/cloud-provisioning/how-to-troubleshoot#object-synchronization-problems)
* [Troubleshooting sync runs that are in quarantine](https://docs.microsoft.com/azure/active-directory/cloud-provisioning/how-to-troubleshoot#provisioning-quarantined-problems)
