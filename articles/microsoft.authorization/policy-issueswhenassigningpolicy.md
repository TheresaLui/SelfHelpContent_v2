<properties
    pageTitle="Issues when assigning a policy"
    description="Issues when assigning a policy"
    service="microsoft.authorization"
    resource="policyDefinitions"
    authors="robga"
    ms.author="robga"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32739635"
    resourceTags=""
    productPesIds="16456"
    cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
    articleId="4b8e9727-d00c-4dd1-bd7a-456684212083"
    ownershipId="Compute_AzurePolicy"
/>

# Azure Policy - Issues when assigning a policy

## **Recommended Steps**

* **Policy assignment issues**

Please allow up to _30 minutes_ for a [policy assignment](https://docs.microsoft.com/azure/governance/policy/concepts/assignment-structure) to take into effect. You can log out and log back in which will trigger a cache refresh for a policy assignment to take into effect. You can assign a policy using the [Azure Portal](https://docs.microsoft.com/azure/governance/policy/assign-policy-portal), [PowerShell](https://docs.microsoft.com/azure/governance/policy/assign-policy-powershell), [Azure CLI](https://docs.microsoft.com/azure/governance/policy/assign-policy-azurecli) and [Azure Resource Manager template](https://docs.microsoft.com/azure/governance/policy/assign-policy-template).

* **Parameter issues**

Parameters within a policy assignment gives the values to those defined in the definition. More information about parameters can be found [here](https://docs.microsoft.com/azure/governance/policy/concepts/definition-structure#parameters). We recommend having a default value for parameters to ensure proper application.
To understand compliance results of a parameter better, please refer to this [documentation](https://docs.microsoft.com/azure/governance/policy/how-to/determine-non-compliance#compliance-details).

* **Issues with assigning the policy definition cross-subscriptions**

You can only assign policy definitions to a given scope or its children. For example, if you have Subscription A and B, policies defined in A can only be applied to A and resource groups/resources below. You cannot apply the definition to B. To assign definitions cross subscriptions, create the definition at a Management Group Level. For information on management groups, please refer [here](https://docs.microsoft.com/azure/governance/management-groups/overview).

## **Recommended Documents**

* [Understanding Assignment structure](https://docs.microsoft.com/azure/governance/policy/concepts/assignment-structure)
* [Assign a policy programmatically](https://docs.microsoft.com/azure/governance/policy/how-to/programmatically-create#create-and-assign-a-policy-definition)
* [Parameters within an assignment](https://docs.microsoft.com/azure/governance/policy/concepts/assignment-structure#parameters)
* [Author policies for parameter arrays](https://docs.microsoft.com/azure/governance/policy/how-to/author-policies-for-arrays#parameter-arrays)
* [Get compliance data](https://docs.microsoft.com/azure/governance/policy/how-to/get-compliance-data)
* [Parameters when creating a custom definition](https://docs.microsoft.com/azure/governance/policy/tutorials/create-custom-policy-definition#parameters)
* [Sample Policy Definition with array parameters](https://docs.microsoft.com/azure/governance/policy/samples/allowed-locations)
* [Check condition using count](https://docs.microsoft.com/azure/governance/policy/concepts/definition-structure#count)
