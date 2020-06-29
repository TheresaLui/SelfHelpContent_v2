<properties
    pageTitle="Operation blocked by Policy"
    description="Operation blocked by Policy"
    service="microsoft.authorization"
    resource="policyDefinitions"
    authors="robga"
    ms.author="robga"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32739637"
    resourceTags=""
    productPesIds="16456"
    cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
    articleId="589d49d4-fa38-4826-b386-ea576f4b58a5"
    ownershipId="Compute_AzurePolicy"
/>

# Azure Policy - Operation blocked by Policy

## **Recommended Steps**

* **Denied by Policy**

When you are denied by a policy, the error message will give the policy definition and assignment ID. That ID will point to a assignment and/or definition which should have information needed to be compliant and/or proceed.
If you did not get the ID in the error message, you can refer to the activity log to get that information. Please refer to the policy assignment to see what parameters/restrictions are put into place.

* **Required Roles**

To create, update, or delete a Policy definition or assignment, you must have Owner or Policy Contributor role. To view compliance details, you must have reader role.
