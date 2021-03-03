<properties
  pagetitle="Identity Protection self help guide"
  ms.author="kawilson,elsagie"
  selfhelptype="Generic"
  supporttopicids="32749418"
  resourcetags=""
  productpesids="15947"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="6bc4e686-7ac5-4850-80dc-ac809cf2bee5"
  ownershipid="Azure_Security_Security_Center" />
# Identity Protection self help guide

## MFA recommendations

### The accounts that are shown as "User accounts requiring MFA" are already covered by MFA
There are 3 ways to enforce MFA to be compliant: 
1. By per-user assignment 
2. By Conditional Access (CA) Policy 
3. By Security Defaults 

Are the accounts covered by MFA in any of the 3 ways above? 

### How do I enable Security Defaults on my tenant?
[Enable MFA security defaults](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults?WT.mc_id=Portal-Microsoft_Azure_Security) in Azure Active Directory (included in Azure AD free) 

### How do I set CA policy on the tenant to enforce MFA in order to be compliant?
To [enable MFA using conditional access](https://docs.microsoft.com/azure/active-directory/conditional-access/overview?WT.mc_id=Portal-Microsoft_Azure_Security), you must have an Azure AD Premium license and have AD tenant admin permissions. 

To be MFA compliant, CA Policy should: 
1. Enforce MFA 
2. Include Microsoft Azure Management App Id (797f4846-ba00-4fd7-ba43-dac1f8f63013) or All apps 
3. Not exclude Microsoft Azure Management App Id 

### I already use CA policy to enforce MFA and still get this recommendation
Verify the following: 
- The CA Policy enforces MFA 
- The accounts that are shown as "User accounts requiring MFA" are included/excluded in the MFA CA Policy Users section or are part of one of the groups that are included/excluded in the Groups section 
- Azure Management App Id (797f4846-ba00-4fd7-ba43-dac1f8f63013) or all apps are included in the CA policy Apps sections 
- Azure Management App Id is not excluded in the CA policy Apps section 

### I am using third-party MFA to enforce MFA in my organization
The MFA recommendation doesn't support third-party MFA (for example, DUO). Consider disabling the MFA recommendation if you find it irrelevant. 

### The accounts that are shown as "User accounts requiring MFA" don't have any permissions on the subscription.
Why do I see this?

**"MFA should be enabled on accounts with permissions on your subscription"** recommendations refer to [RBAC](https://docs.microsoft.com/azure/role-based-access-control/role-definitions-list) roles **and** the [Classic administrator](https://docs.microsoft.com/azure/role-based-access-control/classic-administrators) role. Verify that none of the accounts have such roles. 

### I am using PIM in order to enforce MFA. Why PIM accounts are shown as non-compliant?
ASC MFA recommendations currently don't support PIM accounts. You can add these accounts to a CA Policy in the Users/Group section. 

### How can I programmatically query accounts without MFA? 
To query the accounts without MFA, see [Identify accounts without multi-factor authentication MFA enabled](https://docs.microsoft.com/azure/security-center/security-center-identity-access#identify-accounts-without-multi-factor-authentication-mfa-enabled)

### Can I exempt /dismiss some of the accounts? 
The capability to exempt some accounts that don’t use MFA is not currently supported.  
 
## A maximum of 3 owners should be designated for your subscription:  
###  Can I customize the number of owners? 
- Currently, the feature checks for 3 customers, with no ability to change this. This may be open for customization in the future.  
- You can disable the recommendation if it doesn't fit your organization requirements.  
- Deprecated accounts should be removed from your subscription. 

### What does it mean that my account is deprecated?  
Deprecated accounts are accounts that are no longer needed and are blocked from signing in by Azure Active Directory. 

## **Recommended Documents**

* [Protect identity and access](https://docs.microsoft.com/azure/security-center/security-center-identity-access)
* [Security recommendations - a reference guide](https://docs.microsoft.com/azure/security-center/recommendations-reference)
* [Permissions in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-permissions)

### Troubleshooting
* [Azure Security Center Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

### FAQ
* [Azure Security Center FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)
