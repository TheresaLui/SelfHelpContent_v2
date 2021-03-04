<properties
    pageTitle="Troubleshooting conditional access policies in Azure Active Directory"
    description="Troubleshooting conditional access policies in Azure Active Directory"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="marwaIDCXP"
    ms.author="marwa"
    displayOrder="1770"
    supportTopicIds="32596872"
    selfHelpType="generic"
    resourceTags=""
    productPesIds="16579"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    articleId="484b506b-cd37-45aa-b0eb-ea11c390a70b"
    ownershipId="AzureIdentity_MultiFactorAuthentication"
/>

# Troubleshooting conditional access policies in Azure Active Directory

## Resolve problems with the [Sign-in Diagnostic]

You can quickly find out what happened or diagnose problems related to user sign-in by using the [Sign-in Diagnostic](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ConditionalAccessBlade/diagnose)

1. Launch the Sign-in Diagnostic.
2. Find the event to analyze by entering in the details you have about the user, application, time of sign-in, request Id, or correlation Id.
3. Review the diagnostic results showing the details of what happened and what actions you can take to make changes (if any changes are needed).

## **Recommended Steps**

**[Use What-If to troubleshoot Sign-In](https://docs.microsoft.com/azure/active-directory/conditional-access/troubleshoot-conditional-access-what-if)**
1.	Navigate to the Azure AD Sign-in page
2.	Filter sign-ins by user, time range, application, status, client app, and so on
3.	Select a sign-in event and view the Conditional Access tab to see which policies were evaluated
4.	Click on the row of a policy to view the policy details and understand why it applied

**Tools to troubleshoot a Conditional Access policy**
* Report-only mode lets you evaluate a policy without impacting users
* What-if tool lets you simulate sign-in events and see which policies apply
* Insights and reporting workbook displays real-time impact of each policy

## **Recommended Documents**

* [How to best configure your CA policy](https://docs.microsoft.com/azure/active-directory/conditional-access/best-practices)
* [Configure your CA policies using Conditions](https://docs.microsoft.com/azure/active-directory/conditional-access/conditions)
* [Use Customer Controls in CA Policies](https://docs.microsoft.com/azure/active-directory/conditional-access/controls)
* [Build CA Policy based on Locations](https://docs.microsoft.com/azure/active-directory/conditional-access/location-condition)
