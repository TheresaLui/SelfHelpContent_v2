<properties
    pageTitle="Writing a policy definition"
    description="Writing a policy definition"
    service="microsoft.authorization"
    resource="policyDefinitions"
    authors="robga"
    ms.author="robga"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32739640"
    resourceTags=""
    productPesIds="16456"
    cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
    articleId="75db269a-c645-49ae-af74-34de79897a42"
    ownershipId="Compute_AzurePolicy"
/>

# Azure Policy - Writing a policy definition

## **Recommended Steps**

* **Policy definition issues**

Validate that the [definition structure](https://docs.microsoft.com/azure/governance/policy/concepts/definition-structure) is correct
Ensure the [alias](https://docs.microsoft.com/azure/governance/policy/tutorials/create-custom-policy-definition#find-the-property-alias) is mapped to the desired resource type/property and effects are as expected
If you need help creating a custom policy, follow the tutorial found [here](https://docs.microsoft.com/azure/governance/policy/tutorials/create-custom-policy-definition). We recommend writing policy using our [VS Code extension](https://docs.microsoft.com/azure/governance/policy/how-to/extension-for-vscode), which provides alias look-up and syntax highlight.

* **Alias not found/not working**

If an alias is not working, be sure to validate that the [alias](https://docs.microsoft.com/azure/governance/policy/tutorials/create-custom-policy-definition#find-the-property-alias) is correctly mapped to the desire resource type. The easiest way to find an alias is by using our [VS Code extension](https://docs.microsoft.com/azure/governance/policy/how-to/extension-for-vscode) to [hover over a resource property](https://docs.microsoft.com/azure/governance/policy/how-to/extension-for-vscode#discover-aliases-for-resource-properties). Other ways to find an alias found, including commands, are found [here](https://docs.microsoft.com/azure/governance/policy/concepts/definition-structure#aliases). If an alias does not exist, please create a support ticket.

* **Tagging resources using Azure Policy**

Find more information about managing your tags with Azure Policy [here](https://docs.microsoft.com/azure/governance/policy/tutorials/govern-tags).

If you want a policy to add a [tag](https://docs.microsoft.com/rest/api/resources/tags) if one does not exist, but still respect user input, use [Modify](https://docs.microsoft.com/azure/governance/policy/concepts/effects#modify) effect. Policy's Modify effect lets you add, remove, or addOrReplace tags.

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
