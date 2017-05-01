<properties
    pageTitle="I can’t find any data in the Azure Active Directory activity logs I have downloaded"
    description="I can’t find any data in the Azure Active Directory activity logs I have downloaded"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="MarkusVi"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="azureadreports_missingdata_download,azureadrreports_missingdata_audit"
    productPesIds=""
    cloudEnvironments="public"
/>

# I can’t find any data in the Azure Active Directory activity logs I have downloaded

## **Recommended steps**

When you download activity logs in the Azure portal, we limit the scale to 120K records, sorted by most recent.

- You can use the [Azure AD Reporting APIs](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-api-getting-started) to fetch up to a million records at any given point. Our recommended approach is to run a script on a scheduled basis that calls the reporting APIs to fetch records in an incremental fashion over a period of time (e.g., daily or weekly).

## **Recommended documents**
[I can’t find any data in the Azure Active Directory activity logs I have downloaded](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-troubleshoot-missing-data-download)  
[I can’t find some actions that I performed in the Azure Active Directory activity log](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-troubleshoot-missing-audit-data)  
[Azure Active Directory reporting FAQ](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-faq)

