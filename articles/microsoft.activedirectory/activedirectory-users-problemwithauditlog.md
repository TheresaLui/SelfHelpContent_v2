<properties 
    pageTitle="Problem with Azure AD audit logs for a user"
    description="Problem with Azure AD audit logs for a user"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="Jeffsta-MSFT"
    selfHelpType="generic" 
    supportTopicIds="32615469"
    productPesIds="16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
 	articleId="81d12751-6f85-401b-af5c-5d3e867f41d6"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Problem reading Azure AD audit logs for a user

## **Recommended steps**

1. Ensure the activity you are looking for occurred within the audit log retention period. If an event occurred earlier than the beginning of the retention period, the audit log cannot be retrieved by an administrator or by Microsoft Customer Support. The [audit log retention period](https://docs.microsoft.com/azure/active-directory/reports-monitoring/reference-reports-data-retention) is 30 days for organizations with licenses to Azure AD Premium P1 or P2, and 7 days for other customers.<br>
2. Ensure you are authorized to read the audit logs that you are looking for. A Security Administrator, Security Reader, or Global Administrator can read all audit logs for Azure AD. In addition, any user in the directory can read their own audit logs.<br>

## **Recommended documents**

* [Azure AD audit log reference](https://docs.microsoft.com/azure/active-directory/reports-monitoring/reference-audit-activities)<br>
* [Azure AD reporting API](https://docs.microsoft.com/azure/active-directory/reports-monitoring/concept-reporting-api)<br>
