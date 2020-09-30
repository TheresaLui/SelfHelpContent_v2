<properties
    pageTitle="Debugging a policy"
    description="Debugging a policy"
    service="microsoft.authorization"
    resource="policyDefinitions"
    authors="robga"
    ms.author="robga"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32739634"
    resourceTags=""
    productPesIds="16456"
    cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
    articleId="f721247a-1869-402f-93f8-6781c03c44a6"
    ownershipId="Compute_AzurePolicy"
/>

# Azure Policy - Debugging a policy

## **Recommended Steps**

 **Troubleshooting a policy definition/ Help with debugging a policy**

* Be sure to validate that the [alias](https://docs.microsoft.com/azure/governance/policy/tutorials/create-custom-policy-definition#find-the-property-alias) is correct and [effects](https://docs.microsoft.com/azure/governance/policy/concepts/effects) are as expected.
* We do have some [policy known issues](https://github.com/Azure/azure-policy#known-issues), please be sure to take those into consideration when writing a custom policy.
When troubleshooting a policy definition, it is important to have a deployed resource that you expect to compliant and one to be non-compliant. This way you can validate both cases.
* We always recommend starting with an 'Audit' policy to get an assessment of where your environment is before having a strict enforcement.
* A good way to test your policy without affecting your environment is to use [Enforcement Mode](https://docs.microsoft.com/azure/governance/policy/concepts/assignment-structure#enforcement-mode) set to Enabled or Disabled at assignment time.
* Reminder that policy works on an If (this criteria matches) then (take this effect). If you want to deny SQL resources, the if statement should be written 'if SQL then deny'.

You can get a list of policy samples in [our documentation](https://docs.microsoft.com/azure/governance/policy/samples/allowed-locations), [Azure-policy GitHub Repo](https://github.com/Azure/azure-policy) and [Community Policy repo.](https://github.com/Azure/Community-Policy)

## **Recommended Documents**

* [Tutorial for creating a custom policy](https://docs.microsoft.com/azure/governance/policy/tutorials/create-custom-policy-definition)
* [Understanding policy assignment](https://docs.microsoft.com/azure/governance/policy/concepts/assignment-structure)
* [Understanding policy definition](https://docs.microsoft.com/azure/governance/policy/concepts/definition-structure)
* [Evaluate impact of a new policy](https://docs.microsoft.com/azure/governance/policy/concepts/evaluate-impact)
* [Get compliance data](https://docs.microsoft.com/azure/governance/policy/how-to/get-compliance-data)
* [Cause of non-compliance](https://docs.microsoft.com/azure/governance/policy/how-to/determine-non-compliance)
