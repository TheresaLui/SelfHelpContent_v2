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
	supportTopicIds="32684511"
	productPesIds="16666"
	articleId="8d591007-b401-4b63-9f3e-451f17322ef4"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Problems setting up Provisioning Agent

## **Recommended Steps**

* **Provisioning Agent installation is successful, but the service does not startup**

At the end of Provisioning Agent installation, you get the error message "Service *Microsoft Azure AD Connect Provisioning Agent* failed to start. Verify that you have sufficient privileges to start system services."

By default the installer creates a local NT Service Logon Account called **NT SERVICE\AADConnectProvisioningAgent** to start the service. You may have a group policy that prevents local accounts from starting a service.

To resolve this issue, go to the service editor and change the "Logon Account" to a domain admin and restart the service.

* **Provisioning agent is unable to register with Azure AD tenant**

When configuring the Provisioning Agent with your AD domain in the final *Confirm* step, the registration fails with Gateway Timeout error. It is likely that the Windows Server hosting the provisioning agent does not have direct outbound HTTP connect capabilities and it requires connecting using outbound HTTP proxy.

Follow the steps documented in the section [How do I configure the Provisioning Agent to use a proxy server for outbound HTTP communication?](https://docs.microsoft.com/azure/active-directory/saas-apps/workday-inbound-tutorial#how-do-i-configure-the-provisioning-agent-to-use-a-proxy-server-for-outbound-http-communication) to setup internet connectivity using outbound proxy server.

* **Provisioning Agent installation is successful, but registration fails with *Security Error***

Probable cause: The agent is unable to execute the PowerShell registration scripts due to local PowerShell execution policies.

Resolution step: Change the PowerShell execution policies on the server. Set the **Machine and User policies** as "Undefined" or "RemoteSigned".

* **Provisioning Agent is unable to connect to on-premises AD and receives time-out error**

When configuring the Provisioning Agent with your AD domain in the step **Connect Active Directory**, the wizard takes a long time trying to load the AD schema and eventually times out. This error usually shows up if the wizard is unable to contact the AD domain controller server due to firewall issues.

On the **Connect Active Directory** wizard screen, while providing the credentials for your AD domain, there is an option called "Select domain controller priority". Use this option to select a domain controller that is in the same site as the provisioning agent server and ensure that there are no firewall rules blocking the communication.

## **Recommended Documents**

* [Tutorial: Configure Workday for automatic user provisioning](https://docs.microsoft.com/azure/active-directory/saas-apps/workday-inbound-tutorial)
