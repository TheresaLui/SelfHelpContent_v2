<properties
    pageTitle="Conditional Access - Device policy applied to b2b or external user"
    description="Conditional Access - Device policy applied to b2b or external user"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="zachoi"
    ms.author="zachoi"
    displayOrder="1"
    articleId="ISP_ConditionalAccess_ExternalUserDevicePolicy"
	  diagnosticScenario="ConditionalAccess"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_ConditionalAccess"
/>

# Conditional Access Issue Preventing User Sign-In

<!--issueDescription-->

We have detected that a MAM or MDM policy applied to the sign-in associated with Correlation Id <!--$CorrelationId-->[CorrelationId]<!--/$CorrelationId--> coming from a guest/external user. MDM and MAM cannot be satisfied by guest/external users so such policies will always result in a block.

If you don’t want external users to be blocked by your MAM or MDM policy, you should exclude guest users from the policy or require a grant control that they can satisfy, such as multi-factor authentication.

<!--/issueDescription-->

Details: <!--$IssueDetails-->[IssueDetails]<!--/$IssueDetails-->

## **Recommended Documents**

- [Conditional Access for B2B Collaboration Users](https://docs.microsoft.com/azure/active-directory/external-identities/conditional-access)
