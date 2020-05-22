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

## **Recommended Steps**

**Steps to [Troubleshoot a Sign-In](https://docs.microsoft.com/azure/active-directory/conditional-access/troubleshoot-conditional-access-what-if)**
1.	Navigate to the Azure AD Sign-ins page
2.	Filter sign-ins by user, time range, application, status, client app and more
3.	Select a sign-in event and view the Conditional Access tab to see which policies were evaluated
4.	Click on the row of a policy to view the policy details and understand why it applied

**Tools to troubleshoot a Conditional Access policy**
* Report-only mode lets you evaluate a policy without impacting users
* What-if tool lets you simulate sign-in events and see which policies apply
* Insights and reporting workbook displays real-time impact of each policy

**Baseline Protection Policies**
- Baseline Protection policies have been deprecated. They are no longer being enforced and will soon be removed from Azure Portal. We recommend enabling [security defaults](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults) or [configuring equivalent conditional access policies](https://docs.microsoft.com/azure/active-directory/conditional-access/concept-conditional-access-policy-common#typical-policies-deployed-by-organizations) instead. 


## **Recommended Documents**

* [Conditional Access overview](https://docs.microsoft.com/azure/active-directory/conditional-access/overview)
* [Best practices for conditional access in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/conditional-access/best-practices)
* [Conditions in Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/conditions)
* [Controls in Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/controls)
* [Locations in Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/location-condition)
* [How to: Block legacy authentication to Azure AD with conditional access](https://docs.microsoft.com/azure/active-directory/conditional-access/block-legacy-authentication)
