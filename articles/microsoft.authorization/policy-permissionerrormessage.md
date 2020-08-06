<properties
    pageTitle="Permission error message from Policy"
    description="Permission error message from Policy"
    service="microsoft.authorization"
    resource="policyAssignments"
    authors="robga"
    ms.author="robga"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32730234"
    resourceTags=""
    productPesIds="16456"
    cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
    articleId="5a12fb4f-fc19-4cb6-834b-6cc5851a8172"
    ownershipId="Compute_AzurePolicy"
/>

# Azure Policy - Permission error message from Policy

## **Recommended Steps**

* **Denied by Policy**

When you are denied by a policy, the error message will give the policy definition and assignment ID. Please use that ID to get more information from within Policy. If you did not get the ID in the error message, you can refer to the activity log to get that information.

* **Required Roles**

To create, update, or delete a Policy definition or assignment, you must have Owner or Policy Contributor role.
To view compliance details, you must have reader role.

* **Getting the following error on assignment at root Management Group: The current subscription type is not permitted to perform operations on any provider namespace. Please use a different subscription.**

AAD subscription is a special type of subscription that can not contain or operate any Azure resources. Please exclude the subscription from the policy assignment.

* **Getting the following error on Compliance Details: Encountered an error while authoring the client 'clientid' with object id 'objectid' on action 'resourceid/read' over scope 'scopeid'.**

Compliance Details page requires the resource read access. Policy Contributor permission is not sufficient. Please ensure that you have the resource read access. 

## **Recommended Documents**

* [Permissions required for Azure Policy](https://docs.microsoft.com/azure/governance/policy/overview#rbac-permissions-in-azure-policy)
* [Configuring permissions for deployIfNotExists policy](https://docs.microsoft.com/azure/governance/policy/how-to/remediate-resources#configure-policy-definition)