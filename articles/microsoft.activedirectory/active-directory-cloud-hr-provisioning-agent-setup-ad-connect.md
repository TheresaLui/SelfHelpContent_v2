<properties
	pageTitle="Provisioning Agent is unable to connect to on-premises AD and shows time-out error"
	description="Provisioning Agent is unable to connect to on-premises AD and shows time-out error"
	infoBubbleText="Provisioning Agent is unable to connect to on-premises AD and receives time-out error"
	service="microsoft.activedirectory"
	resource="activedirectory"
	authors="cmmdesai"
	ms.author="chmutali"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32629760,32629802"
	productPesIds="16666"
	articleId="8d591007-b474-4b63-9f3e-451f17322ef4"
	CloudEnvironments="Public"
/>

# Provisioning Agent is unable to connect to on-premises AD and receives time-out error

When configuring the Provisioning Agent with your AD domain in the step *Connect Active Directory*, the wizard takes a long time trying to load the AD schema and eventually times out. If you encounter this issue, then follow the recommended steps below.

## Probable Cause

This error usually shows up if the wizard is unable to contact the AD domain controller server due to firewall issues.

## Recommended Steps

On the *Connect Active Directory* wizard screen, while providing the credentials for your AD domain, there is an option called *Select domain controller priority*. Use this option to select a domain controller that is in the same site as the provisioning agent server and ensure that there are no firewall rules blocking the communication.

## Recommended Documents

* [Tutorial: Configure Workday for automatic user provisioning](https://docs.microsoft.com/azure/active-directory/saas-apps/workday-inbound-tutorial)
