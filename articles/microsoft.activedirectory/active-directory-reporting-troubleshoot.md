<properties
    pageTitle="Problem with a specific sign-in log entry"
    description="Azure AD reporting"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="dhanyahk"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32615415"
    resourceTags=""
    productPesIds="16577"
    cloudEnvironments="public"
    />

# Azure AD Sign-in logs

## **Recommended steps**

### **Troubleshooting issues with sign-ins**

* If you have a CorrelationId or RequestId, visit the [Sign-ins blade](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/SignIns) in the Azure portal, filter by "CorrelationId" and look at the Error code and failure reasons.
* If you have the error code, check out the [error description and resolution](https://docs.microsoft.com/azure/active-directory/reports-monitoring/reference-sign-ins-error-codes#error-codes) documentation to determine the cause of the issue.
* If you have issues with multiple sign-in requests, visit the [Sign-ins blade](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/SignIns) in the Azure portal and try filtering by user or application to determine the scope of the issue before filing a support ticket.

If the issue you have with sign-ins is not covered by the above scenarios, please file a support ticket.

## **Recommended documents**

* [Azure AD Activity Logs Retention](https://docs.microsoft.com/azure/active-directory/reports-monitoring/reference-reports-data-retention)<br>
* [Azure AD Activity Logs Latency](https://docs.microsoft.com/azure/active-directory/reports-monitoring/reference-reports-latencies)<br>
* [Azure Active Directory reporting FAQ](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-faq)

