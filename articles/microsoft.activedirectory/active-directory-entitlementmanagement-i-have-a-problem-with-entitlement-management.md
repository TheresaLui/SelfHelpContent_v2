<properties
  pagetitle="I have a problem with Entitlement Management"
  service="microsoft.activedirectory"
  resource="activedirectory"
  ms.author="sbounouh"
  selfhelptype="Generic"
  supporttopicids="32692567"
  resourcetags=""
  productpesids="16577"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec"
  articleid="ed6816a5-dfd0-454c-a8b1-4b4aec1015a0"
  ownershipid="AzureIdentity_ComplianceAndReporting" />
# I have a problem with Entitlement Management

## FAQs
**When should I use Azure AD Entitlement Management, Access Reviews, or Privileged Identity Management (PIM)?**

- These capabilities are all part of Azure AD Identity Governance. Depending on your scenarios, you can use one, or a combination of them. For more information on the scenarios supported by each of Entitlement Management, Access Reviews and PIM, see this [overview page](https://docs.microsoft.com/azure/active-directory/governance/identity-governance-overview).

**How do I automate access package creation?**

1. Make sure you have one of the following required licenses:
    - Azure AD Premium P2
    - Enterprise Mobility + Security (EMS) E5 license
2. Start Microsoft Graph Explorer or Postman, or create your own client app to call Microsoft Graph. To call the Microsoft Graph APIs, you need to use an account with the global administrator role and the appropriate permissions. See [Entitlement Management API documentation](https://docs.microsoft.com/graph/api/resources/entitlementmanagement-root?view=graph-rest-beta) to learn about the required permissions.
3. See [this tutorial](https://docs.microsoft.com/graph/tutorial-access-package-api) for steps on  how to create an access package using Microsoft Graph APIs.
4. For more information about other Entitlement Management APIs, see [Working with the Azure AD entitlement management API](https://docs.microsoft.com/graph/api/resources/entitlementmanagement-root?view=graph-rest-beta).

## **Recommended Steps**

### I have a problem with administrating Entitlement Management

- Follow [these steps](https://docs.microsoft.com/azure/active-directory/governance/entitlement-management-troubleshoot?WT.mc_id=Portal-Microsoft_Azure_Support#administration) to troubleshoot administrative issues.


### I have a problem managing resources

- Follow [these steps](https://docs.microsoft.com/azure/active-directory/governance/entitlement-management-troubleshoot?WT.mc_id=Portal-Microsoft_Azure_Support#resources) to troubleshoot issues related to resources.


### I have a problem managing external users

- Follow [these steps](https://docs.microsoft.com/azure/active-directory/governance/entitlement-management-troubleshoot?WT.mc_id=Portal-Microsoft_Azure_Support#external-users) to troubleshoot issues related to external users.


### I have a problem with requests

- Follow [these steps](https://docs.microsoft.com/azure/active-directory/governance/entitlement-management-troubleshoot?WT.mc_id=Portal-Microsoft_Azure_Support#requests) to troubleshoot issues related to requests.


### I have a problem with policies
- Follow [these steps](https://docs.microsoft.com/azure/active-directory/governance/entitlement-management-troubleshoot?WT.mc_id=Portal-Microsoft_Azure_Support#multiple-policies) to troubleshoot issues when multiple policies apply to a requester.

## **Recommended Documents**

* [Troubleshooting Entitlement Management](https://docs.microsoft.com/azure/active-directory/governance/entitlement-management-troubleshoot)
* [Tutorial: Create an access package using Microsoft Graph APIs](https://docs.microsoft.com/graph/tutorial-access-package-api)
* [Working with the Azure AD entitlement management API](https://docs.microsoft.com/graph/api/resources/entitlementmanagement-root?view=graph-rest-beta)
