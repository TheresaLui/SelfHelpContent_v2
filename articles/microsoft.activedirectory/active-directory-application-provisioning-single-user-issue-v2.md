<properties
	pageTitle="Azure AD user provisioning to SaaS applications - Single user issue"
	description="Azure AD user provisioning to SaaS applications - Single user issue"
	infoBubbleText="Azure AD user provisioning to SaaS applications - Single user issue"
	service="microsoft.activedirectory"
	resource="activedirectory"
	authors="ArvindHarinder1"
	ms.author="ArvindHarinder1"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32684505"
	productPesIds="16666"
	articleId="5d66987d-73a4-4ac9-a1f6-11c732cc61f4"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Provisioning from Azure AD to SaaS (Including SCIM) Apps - Problem affecting a single user
## **Recommended Steps**

* The user/group may not have been provisioned because our service hasn't had a chance to evaluate the user yet. Review the [guidance](https://docs.microsoft.com/azure/active-directory/manage-apps/application-provisioning-when-will-provisioning-finish-specific-user) for how long provisioning takes as well as the [progress bar](https://docs.microsoft.com/azure/active-directory/manage-apps/application-provisioning-when-will-provisioning-finish-specific-user) on the provisioning configuration page. If the steady state specified in the additional details section is before the date the user was created/updated/ deleted, it means we have not evaluated the user yet. In this scenario, the best thing to do is wait for the provisioning service to finish.  
    * Note that our service is only aware of changes to a user/group in the source system (Azure Active Directory). If a user/group is removed directly in the application (e.g. ServiceNow), we are not aware of those changes and do not roll it back based on the state of the user in the source system. In this scenario, it is best to roll back the change directly in the target application. 
* Our service evaluated the user/group and determined it should not be provisioned:

	* If you've set the scope to assigned users and groups, check if the user/group is assigned to the application
	* If the user/group is assigned to the application, ensure that they are not assigned to the default access role. This role cannot be used for provisioning. 
	* If you've set an attribute based scoping filter, ensure that the user meets the criteria that you have specified
	* If users already exist in the target system and the state of the user in the source and target match, we won't take any further action
	
* Our service attempted to provision the user and it failed. For these scenarios, review the troubleshooting and recommendations tab of the provisioning logs:

	* A required attribute on the user might be missing in Azure Active Directory or does not match the format required by the third party application. For example the Country attribute on a user might be set to United States when it should be US. 
    * The attribute is a referential attribute that does not yet exist in the target application. A referential attribute is an attribute that points to another object, e.g. a user that is a member of a group. The user's ID would be in the member attribute of the group, but can only be processed if the user object it points to already exists.

## **Recommended Documents**

* [Check the status of the provisioning job to determine if it has completed](https://docs.microsoft.com/azure/active-directory/manage-apps/application-provisioning-when-will-provisioning-finish-specific-user)
* [Review the provisioning logs for an issue with a specific user / group ](https://docs.microsoft.com/azure/active-directory/reports-monitoring/concept-provisioning-logs)
