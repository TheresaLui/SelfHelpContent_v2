<properties
    pageTitle="Defining and Assigning Policies"
    description="Defining and Assigning Policies"
    service="microsoft.authorization"
    resource="policyAssignments"
    authors="robga"
    ms.author="robga"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32599712"
    resourceTags=""
    productPesIds="16456"
    cloudEnvironments="public"
	articleId="151dbbc0-29a2-4238-ab9b-1edb1cff28b3"
/>

# Azure Policy - Defining and Assigning Policies

## **Recommended Steps**

* **Issues with assigning the policy definition cross-subscription**

The ‘[definition location](https://docs.microsoft.com/azure/governance/policy/concepts/definition-structure#definition-location)’ must be either same or parent level of the assignment. 

* **Issues with Management Group**

You can leverage [Management Group](https://docs.microsoft.com/azure/governance/management-groups/) to assign the same definition across multiple subscriptions.

## **Recommended Documents**

* [Remediate the non-compliant resources](https://docs.microsoft.com/azure/governance/policy/how-to/remediate-resources) 
* [Disable a policy without deleting the assignment](https://docs.microsoft.com/azure/governance/policy/concepts/effects#disabled)
