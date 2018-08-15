<properties
    pageTitle="I can’t find any data in the Azure Active Directory activity logs I have downloaded"
    description="I can’t find any data in the Azure Active Directory activity logs I have downloaded"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="MarkusVi"
    displayOrder="3"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="azureadrreports_missingdata_audit,azureadrreports_missingdata_signin"
    productPesIds=""
    cloudEnvironments="public"
/>

# I can’t find any data in the Azure Active Directory activity logs I have downloaded

## **Recommended steps**

When you download activity logs in the Azure portal, we limit the scale to 120K records, sorted by most recent.

* You can use the [Azure AD Reporting APIs](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-api-getting-started) to fetch up to a million records at any given point. Our recommended approach is to run a script on a scheduled basis that calls the reporting APIs to fetch records in an incremental fashion over a period of time (e.g., daily or weekly).

## **Recommended documents**

* [Azure Active Directory reporting FAQ](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-faq)
