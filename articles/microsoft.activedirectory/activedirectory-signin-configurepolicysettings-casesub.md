<properties
    pageTitle="Configuring new or existing policy settings for Azure Active Directory Services"
    description="Configuring new or existing policy settings for Azure Active Directory Services"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="curtand"
    ms.author="curtand"
    displayOrder="1770"
    supportTopicIds="32596842"
    selfHelpType="generic"
    resourceTags=""
    productPesIds="16579"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    articleId="b797ec2d-c7fb-40ae-8baf-0b6ddcfe0a69"
	ownershipId="AzureIdentity_MultiFactorAuthentication"
/>

# Configuring new or existing policy settings for Azure Active Directory Services

## **Resolve problems with the [Sign-in Diagnostic](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ConditionalAccessBlade/diagnose/symptomId/ms_aad_dxp_signin_caDiagnoseAndSolveSummarySymptom)**
Quickly find out what happened or diagnose problems related to user sign-in by using the [Sign-in Diagnostic](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ConditionalAccessBlade/diagnose/symptomId/ms_aad_dxp_signin_caDiagnoseAndSolveSummarySymptom).  
Steps to use the diagnostic: 
1. Launch the Sign-in Diagnostic.
2. Find the event to analyze by entering in the details you have about the user, application, time of sign-in, request Id, or correlation Id.
3. Review the diagnostic results showing the details of what happened and what actions you can take to make changes (if any changes are needed).
   
## **Recommended Steps**
**Steps to deploy a Conditional Access Policy**

Before you get started, download the step-by-step Conditional Access [Deployment plan](http://aka.ms/conditionalaccessdeploymentplan)
1. [Configure Policy](https://docs.microsoft.com/azure/active-directory/conditional-access/concept-conditional-access-policies), including assignments, conditions, and controls
2. Test policy using [What-if Tool](https://docs.microsoft.com/azure/active-directory/conditional-access/troubleshoot-conditional-access-what-if) and [Report-Only Mode](https://docs.microsoft.com/azure/active-directory/conditional-access/concept-conditional-access-report-only)	
3. [Move to Production](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access)


## **Recommended Documents**

**Getting started with Conditional Access**
* Short intro to Conditional Access [Document](https://docs.microsoft.com/azure/active-directory/conditional-access/overview) and [Video](https://www.youtube.com/watch?v=c_izIRNJNuk)

* [Best Practices](https://docs.microsoft.com/azure/active-directory/conditional-access/best-practices)
	
**Common Conditional Access Policies**
* [Require MFA for Administrators](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-conditional-access-policy-admin-mfa)
* [Block Access by Location](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-conditional-access-policy-location)
* [Block Legacy Authentication](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-conditional-access-policy-block-legacy)
* [Require Compliant Devices](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-conditional-access-policy-compliant-device)
