<properties
    pageTitle="One or more Azure Policy evaluation records (deny action) detected"
    description="One or more Azure Policy evaluation records (deny action) detected"
    service="microsoft.authorization"
    infoBubbleText="One or more Azure Policy evaluation records (deny action) detected. See details on the right."
    diagnosticScenario="AzurePolicyDefiningIssueInsights"
    resource="policyAssignments"
    authors="robga"
    ms.author="robga"
    displayOrder=""
    selfHelpType="diagnostics"
    supportTopicIds=""
    productPesIds="16456"
    cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
    articleId="e9802b12-2126-4064-be9c-edf32897515c"
    ownershipId="Compute_AzurePolicy"
/>

# Azure Policy - One or more Azure Policy evaluation records (deny action) detected

<!--issueDescription-->
Creating an ARM resource or ARM deployment may result in a policy violation.

Here is a list of the policy violations:

<!--$policyAssignmentDetail-->[policyAssignmentDetail]<!--/$policyAssignmentDetail-->
<!--/issueDescription-->

## **Recommended Documents**

* [How frequently does Compliance evaluation run?](https://docs.microsoft.com/azure/governance/policy/how-to/getting-compliance-data#evaluation-triggers)
* [Trigger the re-evaluation](https://docs.microsoft.com/azure/governance/policy/how-to/getting-compliance-data#on-demand-evaluation-scan)
* [Create a custom policy definition](https://docs.microsoft.com/azure/governance/policy/tutorials/create-custom-policy-definition)
* [Troubleshooting a policy definition](https://docs.microsoft.com/azure/governance/policy/how-to/determine-non-compliance)
* [Policy definition structure](https://docs.microsoft.com/azure/governance/policy/concepts/definition-structure)
* [Understanding Policy effects](https://docs.microsoft.com/azure/governance/policy/concepts/effects)
* [Policy sample Github](https://github.com/Azure/azure-policy/tree/master/samples)
* [Issues with assigning the policy definition cross-subscriptions](https://docs.microsoft.com/azure/governance/policy/concepts/definition-structure#definition-location)