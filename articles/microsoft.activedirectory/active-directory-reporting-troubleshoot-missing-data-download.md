<properties
    pageTitle="I can’t find any data in the Azure Active Directory activity logs I have downloaded"
    description="I can’t find any data in the Azure Active Directory activity logs I have downloaded"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="dhanyahk"
    ms.author="curtand"
    displayOrder="3"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="azureadrreports_missingdata_audit,azureadrreports_missingdata_signin"
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="bd14b922-7cde-4bef-bb27-6023a77d124e"
	ownershipId="AzureIdentity_User"
/>

# I can’t find any data in the Azure Active Directory activity logs I have downloaded

## **Recommended Steps**

When you download activity logs in the Azure portal, we limit the scale to 250K records, sorted by most recent. In order to download all the records, you can try the following approaches:

- Use our new **Download** experience in the portal and download up to 250K rows in .csv or JSON format. For more information, see [Download sign-in activities](https://docs.microsoft.com/azure/active-directory/reports-monitoring/concept-sign-ins#download-sign-in-activities).

- You can use the [Azure AD Reporting APIs](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-api-getting-started) to fetch up to a million records at any given point. Our recommended approach is to run a script on a scheduled basis that calls the reporting APIs to fetch records in an incremental fashion over a period of time (for example, daily or weekly).

## **Recommended Documents**

* [Azure Active Directory reporting FAQ](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-faq)
