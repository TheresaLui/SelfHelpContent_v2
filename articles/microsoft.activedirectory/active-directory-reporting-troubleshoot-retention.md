<properties
    pageTitle="How long is report data stored?"
    description="I am unable to see sign-in logs beyond 30 days in my tenant"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="MarkusVi"
    ms.author="markvi"
    displayOrder="4"
    articleId="07b6b188-8986-4d01-87c0-625e6527d083"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="azureadrreports_missingdata_audit,azureadrreports_missingdata_signin"
    productPesIds=""
    cloudEnvironments="public,Fairfax, usnat, ussec"
    ownershipId="AzureIdentity_User"
    />

# I can't see some report data

Common solutions for:

* I can't see more than 30 days of report data
* I can't see data since I switched licenses *n* days ago (changed license SKU from Free to P1 or P2)

## **Recommended Steps**

Depending on your license, Azure Active Directory Actions stores activity reports for the following durations:

| Report           | &nbsp; |  Azure AD Free | Azure AD Premium P1 | Azure AD Premium P2 |
| ---              | ----   |  ---           | ---                 | ---                 |
| Directory Audit  | &nbsp; |    7 days      | 30 days             | 30 days             |
| Sign-in Activity | &nbsp; |    7 days      | 30 days             | 30 days             |

**Note**:  When you change licenses, the amount of data you see (length of storage) is effective from the day you switched licenses. For example, if your Azure AD organization had the Azure AD Free license plan and switched to P1, we start storing your report data from that point onwards. In that case, you wouldn't immediately see "last 30 days" worth of data.

### What if you need data beyond 30 days

* We highly recommend that you configure [Azure Monitor for Azure AD Logs](https://docs.microsoft.com/azure/active-directory/reports-monitoring/concept-activity-logs-azure-monitor) from the time you start using Azure AD services. This way, you can control how long you store the data.
* Depending on your requirements, you can decide which routing option is best for you. For more tips on best practices, check out our [deployment plan](https://docs.microsoft.com/azure/active-directory/reports-monitoring/plan-monitoring-and-reporting) for managing your logs.

## **Recommended Documents**

* [Azure Active Directory report retention policies](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-retention)  
* [Getting started with the reporting API](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-api-getting-started)  
* [Reporting and Monitoring Deployment plan](https://docs.microsoft.com/azure/active-directory/reports-monitoring/plan-monitoring-and-reporting) 
* [Azure Monitor for Azure AD Logs](https://docs.microsoft.com/azure/active-directory/reports-monitoring/concept-activity-logs-azure-monitor)

