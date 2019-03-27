<properties
	pageTitle="Provisioning agent is unable to register with Azure AD tenant"
	description="Provisioning agent is unable to register with Azure AD tenant"
	infoBubbleText="Provisioning agent is unable to register with Azure AD tenant"
	service="microsoft.activedirectory"
	resource="activedirectory"
	authors="cmmdesai"
	ms.author="chmutali"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32629802"
	productPesIds="16666"
	articleId="8d591007-b474-4b63-9f3e-451f17322ef4"
	CloudEnvironments="Public"
/>

# Provisioning agent is unable to register with Azure AD tenant

When configuring the Provisioning Agent with your AD domain in the final *Confirm* step, the registration fails with Gateway Timeout error.  

## Probable Cause

It is likely that the Windows Server hosting the provisioning agent does not have direct outbound HTTP connect capabilities and it requires connecting using outbound HTTP proxy.

## Recommended Steps

follow the steps documented in the section [How do I configure the Provisioning Agent to use a proxy server for outbound HTTP communication?](https://docs.microsoft.com/azure/active-directory/saas-apps/workday-inbound-tutorial#how-do-i-configure-the-provisioning-agent-to-use-a-proxy-server-for-outbound-http-communication) to setup internet connectivity using outbound proxy server.

## Recommended Documents

* [Tutorial: Configure Workday for automatic user provisioning](https://docs.microsoft.com/azure/active-directory/saas-apps/workday-inbound-tutorial)
