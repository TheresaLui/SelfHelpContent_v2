<properties
	pageTitle="Troubleshoot Health service data not up to date"
	description="Azure AD Connect Health self help"
	service="microsoft.aad"
	resource="Microsoft_Azure_ADHybridHealth"
	authors="arluca"
	displayOrder="200"
	selfHelpType="resource"
	cloudEnvironments="public"
/>
# Troubleshoot Health service data not up to date

## **Recommended steps**
1.	Ensure the required endpoints are enabled, and not blocked due to firewall. See [requirements](http://aka.ms/aadchprereqs) section for details. 
2.	Data upload can fail due to outbound communication being subjected to SSL inspection by the network layer. 
3.	You can use the [built-in agent connectivity tool](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-agent-install#test-connectivity-to-azure-ad-connect-health-service).
4.	Ensure [proxy settings](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-agent-install##configure-azure-ad-connect-health-agents-to-use-http-proxy) have been properly configured if applicable.

## **Recommended documents**
* [Common installation questions](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-faq#installation-questions)
