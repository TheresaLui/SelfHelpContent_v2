<properties
    pageTitle="Policy definition basics"
    description="Policy definition basics"
    service="microsoft.authorization"
    resource="policyDefinitions"
    authors="robga"
    ms.author="robga"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32730238"
    resourceTags=""
    productPesIds="16456"
    cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
    articleId="7fbc954e-e95a-42dc-9e26-cd7d852bf570"
    ownershipId="Compute_AzurePolicy"
/>

# Azure Policy - Policy definition basics

## **Recommended Steps**

* **Is this a policy definition issue?**

If you need help creating a custom policy, follow the tutorial found [here](https://docs.microsoft.com/azure/governance/policy/tutorials/create-custom-policy-definition). We recommend writing policy using our [VS Code extension](https://docs.microsoft.com/azure/governance/policy/how-to/extension-for-vscode), which provides aliases look-up and syntax highlight.  
Be sure to validate that the [aliases](https://docs.microsoft.com/azure/governance/policy/tutorials/create-custom-policy-definition#find-the-property-alias) is correctly mapped to the resource type and [effects](https://docs.microsoft.com/azure/governance/policy/concepts/effects) are as expected.


* **Aliases are not found/not working?**

If an aliases is not working, be sure to validate that the [aliases](https://docs.microsoft.com/azure/governance/policy/tutorials/create-custom-policy-definition#find-the-property-alias) exist and is correct. The easiest way to find an aliases is by using our [VS Code extension](https://docs.microsoft.com/azure/governance/policy/how-to/extension-for-vscode) to hover over a resource property.  
If an alias does not exist, create a support ticket. 

* **Is this a issue with tagging resources using Azure Policy?**

Find more information about managing your tags with Azure Policy [here](https://docs.microsoft.com/azure/governance/policy/tutorials/govern-tags).  
If you want to a policy to add a [tag](https://docs.microsoft.com/rest/api/resources/tags) if one does not exist, but still respect user input, use [Modify](https://docs.microsoft.com/azure/governance/policy/concepts/effects#modify) effect. Policys Modify effect lets you add, remove, or addOrReplace tags. It will not make changes to tags that already exist.  
You can get a list of policy samples in [our documentation](https://docs.microsoft.com/azure/governance/policy/samples/allowed-locations), [Azure-policy GitHub Repo](https://github.com/Azure/azure-policy) and [Community Policy repo](https://github.com/Azure/Community-Policy). 

## **Recommended Documents**

* [Understanding Policy effects](https://docs.microsoft.com/azure/governance/policy/concepts/effects)
* [Understanding Policy Modes](https://docs.microsoft.com/azure/governance/policy/concepts/definition-structure#mode)
* [Check conditions using value](https://docs.microsoft.com/azure/governance/policy/concepts/definition-structure#value)
* [Check condition using count](https://docs.microsoft.com/azure/governance/policy/concepts/definition-structure#count)
* [Parameters when creating a custom definition](https://docs.microsoft.com/azure/governance/policy/tutorials/create-custom-policy-definition#parameters)
* [Author policies for parameter arrays](https://docs.microsoft.com/azure/governance/policy/how-to/author-policies-for-arrays#parameter-arrays)
* [Sample Policy Definition with array parameters](https://docs.microsoft.com/azure/governance/policy/samples/allowed-locations)
* [Remediate resources](https://docs.microsoft.com/azure/governance/policy/how-to/remediate-resources)
