<properties
    pageTitle="Conditional Access - Legacy authentication preventing user sign-in"
    description="Conditional Access - Legacy authentication supported preventing user sign-in"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="jeslin"
    ms.author="jeslin"
    displayOrder="1"
    articleId="ISP_ConditionalAccess_LegacyAuthentication"
	  diagnosticScenario="ConditionalAccess"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_B2B"
/>

# Conditional Access Issue Preventing User Sign-In

<!--issueDescription-->

The sign-in <!--$CorrelationId-->[CorrelationId]<!--/$CorrelationId--> used legacy authentication, which can impact the behavior of Conditional Access policies. Consider blocking legacy authentication using a conditional access policy. By default, conditional access policies do not apply to legacy authentication. If access is unexpected with your current policies, set the **client apps** conditions to include **other clients**.

<!--/issueDescription-->

## **Recommended Documents**

- [Configure Legacy Authentication](https://docs.microsoft.com/azure/active-directory/conditional-access/conditions#legacy-authentication)
