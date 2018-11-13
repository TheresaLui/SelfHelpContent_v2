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

| Report           | &nbsp; |  Azure AD Free | Azure AD Premium P1 | Azure AD Premium P2 |
| ---              | ----   |  ---           | ---                 | ---                 |
| Directory Audit  | &nbsp; |	7 days	   | 30 days             | 30 days             |
| Sign-in Activity | &nbsp; | Not available\*| 30 days	         | 30 days             |

\*Sign-in activity is available for 7 days from the individual user profile only. 

If you need data for longer than 30 days, you can pull the data programmatically using the reporting API and store it on your side. Alternatively, you can integrate audit logs into your SIEM systems.

## **Recommended documents**

- [Azure Active Directory report retention policies](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-retention)<br>
- [Getting started with the reporting API](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-api-getting-started)<br>
- [Azure Active Directory reporting FAQ](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-faq)