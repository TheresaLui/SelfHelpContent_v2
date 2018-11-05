<properties
    pageTitle="Azure AD audit Log and activity reports"
    description="Azure AD reporting"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="MarkusVi"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32574686"
    resourceTags=""
    productPesIds="14785,16577"
    cloudEnvironments="public"
    />

# Troubleshooting issues with Sign-ins

## **Recommended steps**

* If you have a CorrelationId or RequestId, visit [Sign-ins Activity logs](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/SignIns) in the Azure Portal, filter by "CorrelationId" and look at the Error code and failure reasons.
* If you have the error code, check out the [error description and resolution](https://docs.microsoft.com/azure/active-directory/reports-monitoring/reference-sign-ins-error-codes#error-codes) documentation to determine the cause of the issue.
* If you have issues with multiple sign-in requests, visit [Sign-ins Activity logs](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/SignIns) in the Azure Portal and try filtering by user or application to determine the scope of the issue before filing a support ticket.

If the issues you have sign-ins is generic, please file a support ticket.

## **Recommended documents**

* [Azure AD Activity Logs Retention](https://docs.microsoft.com/azure/active-directory/reports-monitoring/reference-reports-data-retention)  
* [Azure AD Activity Logs Latency](https://docs.microsoft.com/azure/active-directory/reports-monitoring/reference-reports-latencies)  
* [Azure Active Directory reporting FAQ](https://docs.microsoft.com/azure/active-directory/reports-monitoring/reports-faq)