<properties
    pageTitle="Problem with data retention"
    description="Azure AD reporting"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="dhanyahk"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32615419"
    resourceTags=""
    productPesIds="16577"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="b2de7104-84b1-488e-b270-5cf890e878ec"
	ownershipId="AzureIdentity_ComplianceAndReporting"
/>

# Azure AD Audit Logs

## **Recommended steps**

* You can only see the last 30 days of data if your tenant has an Azure AD Premium license (Azure AD P1 or P2) or last 7 days of data if your tenant has an Azure AD Free or Basic license.<br>
* Sign-in logs are available only for Azure AD Premium tenants. They're not available for Free or Basic licensed tenants.

### **Troubleshooting issues with Sign-ins**

* If you can't see audit logs in your Azure AD Premium P1 tenant, check out our [latency information](https://docs.microsoft.com/azure/active-directory/reports-monitoring/reference-reports-latencies) and file a support ticket if the delay exceeds the documented latency.

## **Recommended documents**

* [Azure AD Activity Logs Retention](https://docs.microsoft.com/azure/active-directory/reports-monitoring/reference-reports-data-retention)<br>
* [Azure AD Activity Logs Latency](https://docs.microsoft.com/azure/active-directory/reports-monitoring/reference-reports-latencies)<br>
* [Azure Active Directory reporting FAQ](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-faq)
