<properties
  pageTitle="I'm having issues around configuring user groups"
  description="I'm having issues around configuring user groups"
  infoBubbleText=""
  service="microsoft.mcas"
  resource=""
  authors="shsagir"
  ms.author="shsagir"
  displayOrder=""
  articleId="mcas-portal-user-groups"
  diagnosticScenario=""
  selfHelpType="generic"
  supportTopicIds="32729006"
  resourceTags=""
  productPesIds="16031"
  ownershipId="CloudAppSecurity_Portal"
  cloudEnvironments="public, fairfax, usnat, ussec"
/>

# I'm having issues around configuring user groups

Most users are able to user group configuration issues using the steps below.

## **Recommended Steps**

* If you have recently added the imported group and you don't see the correct number of members, wait up to 90 minutes for the group to populate
* After this period, if the number of users in the group is 0 or doesn't match to the number of users in the Azure Active Directory (AD) group, proceed to a support case
* If your issue relates to Cloud App Security only monitoring specific groups, check your [scoped deployment](https://docs.microsoft.com/cloud-app-security/scoped-deployment) configuration.

    **Note**: A scoped deployment rule cannot be edited if an imported group included in the rule is deleted in Azure AD. Therefore, to safely remove groups from Azure AD, first remove the imported groups from all scoped deployment rules and then delete the group from Azure AD.  
   
* If you have already removed a group from Azure AD before removing it from all scoped deployment rules, proceed to open a support ticket and provide a list of the affected scoped deployment rules and the group's name.

## **Recommended Documents**

- [Importing user groups from connected apps](https://docs.microsoft.com/cloud-app-security/user-groups)
- [Activity privacy](https://docs.microsoft.com/cloud-app-security/activity-privacy)

If you're still experiencing the issue after reviewing the documentation and configuration, please continue with opening the ticket.
