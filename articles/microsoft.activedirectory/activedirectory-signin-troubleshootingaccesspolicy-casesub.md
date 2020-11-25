<properties
    pageTitle="Troubleshooting conditional access policies in Azure Active Directory"
    description="Troubleshooting conditional access policies in Azure Active Directory"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="curtand"
    ms.author="curtand"
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

### Resolve problems with the [Sign-in Diagnostic](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/diagnose/symptomId/ms_aad_dxp_signin_caDiagnoseAndSolveSummarySymptom)

You can quickly find out what happened or diagnose problems related to user sign-in by using the [Sign-in Diagnostic](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/diagnose/symptomId/ms_aad_dxp_signin_caDiagnoseAndSolveSummarySymptom):

1. Launch the Sign-in Diagnostic.
2. Find the event to analyze by entering in the details you have about the user, application, time of sign-in, request Id, or correlation Id.
3. Review the diagnostic results showing the details of what happened and what actions you can take to make changes (if any changes are needed).

## **Recommended Steps**

**Steps to [Troubleshoot a Sign-In](https://docs.microsoft.com/azure/active-directory/conditional-access/troubleshoot-conditional-access-what-if)**
1.	Navigate to the Azure AD Sign-in page
2.	Filter sign-ins by user, time range, application, status, client app, and so on
3.	Select a sign-in event and view the Conditional Access tab to see which policies were evaluated
4.	Click on the row of a policy to view the policy details and understand why it applied

**Tools to troubleshoot a Conditional Access policy**
* Report-only mode lets you evaluate a policy without impacting users
* What-if tool lets you simulate sign-in events and see which policies apply
* Insights and reporting workbook displays real-time impact of each policy

**Baseline Protection Policies**
- Baseline Protection policies have been deprecated. They are no longer being enforced and will soon be removed from Azure portal. We recommend enabling [security defaults](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults)


## **Recommended Documents**

* [Best practices for conditional access in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/conditional-access/best-practices)
* [Conditions in Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/conditions)
* [Controls in Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/controls)
* [Locations in Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/location-condition)
