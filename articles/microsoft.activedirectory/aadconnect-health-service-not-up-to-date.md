<properties
	pageTitle="Azure AD Connect Health Service is not up to date"
	description="Azure AD Connect Health Service is not up to date"
	infoBubbleText="Azure AD Connect Health Service is not up to date"
	service="microsoft.aad"
	resource="Microsoft_Azure_ADHybridHealth"
	ms.author="janelg"
	displayOrder=""
	articleId="835c60f0-2ab5-4ac8-ace7-847ec21040a3"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629813"
	resourceTags=""
	productPesIds="16577"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_ComplianceAndReporting"
/>

# Azure AD Connect Health Service is not up to date

The Health service data alert occurs when the Azure AD Connect service does not receive data from an agent on the on-premises machine, and the information the portal presents is stale.  To resolve this issue, follow the set of basic checks that may be causing this alert:

## **Recommended Steps**

1. Make sure the latest versions of the agents are installed. View [release history](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-health-version-history).
2. Make sure that Azure AD Connect Health Agents services are **running** on the machine. For example, Connect Health for AD FS should have three services. 
3. Ensure all [requirements](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-health-agent-install#requirements) are met
4. Use [test connectivity tool](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-health-agent-install#test-connectivity-to-azure-ad-connect-health-service) to discover connectivity issues
5. If you have an HTTP Proxy, follow these [configuration steps](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-health-agent-install#configure-azure-ad-connect-health-agents-to-use-http-proxy) 
 
## **Recommended Documents** 

- [Troubleshoot "Health Service Data Not Up To Date" Error](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-health-data-freshness#:~:text=If%20the%20service%20does%20not%20receive%20data%20from,received%20complete%20data%20in%20the%20past%20two%20hours)
