<properties
    pageTitle="One or more errors detected during creation of an Azure Policy Definition"
    description="One or more errors detected during creation of an Azure Policy Definition"
    service="microsoft.authorization"
    infoBubbleText="One or more errors detected during creation of an Azure Policy Definition. See details on the right."
    diagnosticScenario="AzurePolicyDefiningIssueInsights"
    resource="policyDefinitions"
    authors="robga"
    ms.author="robga"
    displayOrder=""
    selfHelpType="diagnostics"
    supportTopicIds=""
    productPesIds="16456"
    cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
    articleId="21fcaa7d-e41b-4d47-8a5a-843ea71bdda0"
    ownershipId="Compute_AzurePolicy"
/>

# Azure Policy - One or more errors detected during creation of an Azure Policy Definition

<!--issueDescription-->
We found the following policy definition syntax errors:

<!--$ErrorMessages-->[ErrorMessages]<!--/$ErrorMessages-->
<!--/issueDescription-->

## Recommended Steps

**Is this a tagging or location policy?**

* [Policy definition must use mode=indexed to only affect appropriate resources](https://docs.microsoft.com/azure/governance/policy/concepts/definition-structure#mode)

**Is this a built-in policy or initiative?**

* [Understanding Enable Monitoring using Azure Security Center initiative](https://docs.microsoft.com/azure/security-center/tutorial-security-policy)
* [Understanding Policy effects](https://docs.microsoft.com/azure/governance/policy/concepts/effects)

**Is this a custom policy?**

* [Troubleshooting a policy definition](https://docs.microsoft.com/azure/governance/policy/how-to/determine-non-compliance)
* [Understanding Policy effects](https://docs.microsoft.com/azure/governance/policy/concepts/effects)

## **Recommended Documents**

* [Create a custom policy definition](https://docs.microsoft.com/azure/governance/policy/tutorials/create-custom-policy-definition)
* [Troubleshooting a policy definition](https://docs.microsoft.com/azure/governance/policy/how-to/determine-non-compliance)
* [Policy definition structure](https://docs.microsoft.com/azure/governance/policy/concepts/definition-structure)
* [Understanding Policy effects](https://docs.microsoft.com/azure/governance/policy/concepts/effects)
* [Policy sample Github](https://github.com/Azure/azure-policy/tree/master/samples)
