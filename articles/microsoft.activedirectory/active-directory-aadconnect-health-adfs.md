<properties
	pageTitle="Azure AD Connect Health"
	description="Azure AD Connect Health for AD FS self help"
	service="microsoft.aad"
	resource="Microsoft_Azure_ADHybridHealth"
	authors="zhiweiw"
	ms.author="zhiweiw"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32574685,32629811,32629816"
	resourceTags=""
	productPesIds="16579,16577"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="f50978b3-d063-4265-aac5-ed839f44856b"
	ownershipId="AzureIdentity_MultiFactorAuthentication"
/>

# Connect Health for AD FS

## **Recommended Steps**

### Troubleshooting registration failures

1.	Ensure you are authorized to perform the operation. Global Admins have access by default. Additionally, you can use [Role Based Access Control](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-operations#manage-access-with-role-based-access-control) to delegate registration permission to Contributor.
2.	Ensure the required endpoints are enabled, and not blocked due to firewall. See [requirements](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-health-agent-install) section for details.
3.	Registration can fail due to outbound communication being subjected to SSL inspection by the network layer

### Troubleshooting Health Service data not up to date

* Follow the steps in the [public documentation for this alert](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-health-data-freshness)

### Troubleshooting AD FS related alerts

* Follow the steps in [catalog documents](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-health-alert-catalog) and corresponding resolutions

### Troubleshooting duplicate servers in the portal

1.	When an agent is removed from the server, the server is not automatically removed from the portal. Duplicate servers will occur, when a second agent is registered by a server with same name/details.
2.	To delete a server from the portal, see [deleting a server or service instance](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-health-operations#delete-a-server-or-service-instance)

## **Recommended Documents**

* [Common installation questions](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-health-faq)<br>
* [Enabling notifications for Alerts](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-health-operations#enable-email-notifications)
