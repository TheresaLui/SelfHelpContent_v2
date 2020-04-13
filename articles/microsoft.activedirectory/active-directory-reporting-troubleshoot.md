<properties
    pageTitle="Problem with a specific sign-in log entry"
    description="Azure AD reporting"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="dhanyahk"
    ms.author="curtand"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32615415"
    resourceTags=""
    productPesIds="16577"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="2c6fef6a-4d9d-4380-8808-758d80d17814"
    	ownershipId="AzureIdentity_ComplianceAndReporting"
/>

# Azure AD Sign-in logs

## **Recommended Steps**

### **Troubleshooting issues with Sign-ins**

- If you have a CorrelationId or RequestId, visit [Sign-ins Activity logs](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/SignIns) in the Azure portal, filter by "CorrelationId" and look at the Error code and failure reasons
- If you have the error code, check out the [error description and resolution](https://docs.microsoft.com/azure/active-directory/reports-monitoring/reference-sign-ins-error-codes#error-codes) documentation to determine the cause of the issue.<br>
- If you have issues with multiple sign-in requests, visit [Sign-ins Activity logs](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/SignIns) in the Azure portal and try filtering by user or application to determine the scope of the issue before filing a support ticket
If the issues you have sign-ins is generic, please file a support ticket

## **Recommended Documents**

- [Azure AD Activity Logs Retention](https://docs.microsoft.com/azure/active-directory/reports-monitoring/reference-reports-data-retention)<br>
- [Azure AD Activity Logs Latency](https://docs.microsoft.com/azure/active-directory/reports-monitoring/reference-reports-latencies)  


