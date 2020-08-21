<properties
    pageTitle="Azure AD Connect Health"
    description="Azure AD Connect Health for AD DS self help"
    service="microsoft.aad"
    resource="Microsoft_Azure_ADHybridHealth"
    authors="arluca"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32574684"
    resourceTags=""
    productPesIds="14785,16577"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="9ad3d4ec-acde-408a-85e8-400a5c632d82"
	ownershipId="AzureIdentity_ComplianceAndReporting"
/>

# Connect Health for AD DS

## **Recommended steps**
### Troubleshooting registration failures

1. Ensure you are authorized to perform the operation. Global Administrators have access by default. Additionally, you can use [Role Based Access Control](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-operations#manage-access-with-role-based-access-control) to delegate registration permission to Contributer.
2. Ensure the required endpoints are enabled, and not blocked due to firewall. See [requirements](http://aka.ms/aadchprereqs) section for details. 
3. Registration can fail due to outbound communication being subjected to SSL inspection by the network layer.

### Troubleshooting Health Service data not up to date

1. Ensure the required endpoints are enabled, and not blocked due to firewall. See [requirements](http://aka.ms/aadchprereqs) section for details. 
2. Data upload can fail due to outbound communication being subjected to SSL inspection by the network layer.
3. You can use the [built-in agent connectivity tool](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-agent-install#test-connectivity-to-azure-ad-connect-health-service).
4. Ensure [proxy settings](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-agent-install##configure-azure-ad-connect-health-agents-to-use-http-proxy) have been properly configured if applicable.

### Troubleshooting duplicate servers in the portal

1. When an agent is removed from the server, the server is not automatically removed from the portal. Duplicate servers will occur, when a second agent is registered by a server with same name/details.
2. To delete a server from the portal, see [deleting a server or service instance](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-operations#delete-a-server-or-service-instance).

## **Recommended documents**

* [Common installation questions](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-health-faq)<br>
* [Enabling notifications for Alerts](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-operations#enable-email-notifications)
