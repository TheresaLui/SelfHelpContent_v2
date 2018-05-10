<properties
    pageTitle="I can't see more than 30 days of report data "
    description="How can I see more than 30 days of report data?"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="MarkusVi"
    displayOrder="4"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="azureadrreports_missingdata_audit,azureadrreports_missingdata_signin"
    productPesIds=""
    cloudEnvironments="public"
/>

# I can't see more than 30 days of report data

## **Recommended steps**

Depending on your license, Azure Active Directory Actions stores activity reports for the following durations:

| Report           | Azure AD Free | Azure AD Premium P1 | Azure AD Premium P2 |
| ---              | ---           | ---                 | ---                 |
| Directory Audit  |	7 days	   | 30 days             | 30 days             |
| Sign-in Activity | Not available*| 30 days	         | 30 days             |

* Sign-in activity is available for 7 days from the individual user profile blade only. You can access individual user sign-ins. 

If you need data for duration that is longer than 30 days, you can pull the data programmatically using the reporting API and store it on your side. Alternatively, you can integrate audit logs into your SIEM systems.



## **Recommended documents**

- [Azure Active Directory report retention policies](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-retention)  
- [Getting started with the reporting API](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-api-getting-started)  
- [Azure Active Directory reporting FAQ](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-faq)

