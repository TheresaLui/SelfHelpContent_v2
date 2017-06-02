<properties
	pageTitle="Agent Registration Failures"
	description="Azure AD Connect Health self help"
	service="microsoft.aad"
	resource="Microsoft_Azure_ADHybridHealth"
	authors="arluca"
	displayOrder="100"
	selfHelpType="resource"
	cloudEnvironments="public"
/>
# Agent registration failures

## **Recommended steps**
1.	Ensure you are authorized to perform the operation. Global Admins have access by default. Additionally, you can use [Role Based Access Control](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-operations#manage-access-with-role-based-access-control) to delegate registration permission to Contributer.
2.	Ensure the required endpoints are enabled, and not blocked due to firewall. See [requirements](http://aka.ms/aadchprereqs) section for details. 
3.	Registration can fail due to outbound communication being subjected to SSL inspection by the network layer. 

## **Recommended documents**
* [Common installation questions](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-faq#installation-questions)
