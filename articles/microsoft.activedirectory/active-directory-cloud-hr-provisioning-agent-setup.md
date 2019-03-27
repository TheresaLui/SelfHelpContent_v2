<properties
	pageTitle="Problems setting up Provisioning Agent"
	description="Problems setting up Provisioning Agent"
	infoBubbleText="Problems setting up Provisioning Agent"
	service="microsoft.activedirectory"
	resource="activedirectory"
	authors="cmmdesai"
	ms.author="chmutali"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32629802"
	productPesIds="16666"
	articleId="8d591007-b401-4b63-9f3e-451f17322ef4"
	CloudEnvironments="Public"
/>

# Problems setting up Provisioning Agent

## **Recommended Steps**

**Provisioning agent is unable to register with Azure AD tenant**

When configuring the Provisioning Agent with your AD domain in the final *Confirm* step, the registration fails with Gateway Timeout error. It is likely that the Windows Server hosting the provisioning agent does not have direct outbound HTTP connect capabilities and it requires connecting using outbound HTTP proxy.

Follow the steps documented in the section [How do I configure the Provisioning Agent to use a proxy server for outbound HTTP communication?](https://docs.microsoft.com/azure/active-directory/saas-apps/workday-inbound-tutorial#how-do-i-configure-the-provisioning-agent-to-use-a-proxy-server-for-outbound-http-communication) to setup internet connectivity using outbound proxy server.

**Provisioning Agent is unable to connect to on-premises AD and receives time-out error**

When configuring the Provisioning Agent with your AD domain in the step **Connect Active Directory**, the wizard takes a long time trying to load the AD schema and eventually times out. This error usually shows up if the wizard is unable to contact the AD domain controller server due to firewall issues.

On the **Connect Active Directory** wizard screen, while providing the credentials for your AD domain, there is an option called "Select domain controller priority". Use this option to select a domain controller that is in the same site as the provisioning agent server and ensure that there are no firewall rules blocking the communication.

## **Recommended Documents**

* [Tutorial: Configure Workday for automatic user provisioning](https://docs.microsoft.com/azure/active-directory/saas-apps/workday-inbound-tutorial)
