<properties
	pageTitle="Provisioning from Cloud HR to AD or Azure AD - Single user issue"
	description="Provisioning from Cloud HR to AD or Azure AD - Single user issue"
	infoBubbleText="Provisioning from Cloud HR to AD or Azure AD - Single user issue"
	service="microsoft.activedirectory"
	resource="activedirectory"
	authors="cmmdesai"
	ms.author="chmutali"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32684506"
	productPesIds="16666"
	articleId="192c51a9-3c9f-43b2-ac86-c5663ee3b916"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Provisioning from Cloud HR to on-premises Active Directory/Azure AD - Problem affecting a single user

Review the steps below to diagnose a problem affecting a single user.

## **Recommended Steps**

* The user may not have been provisioned because the service hasn't had a chance to evaluate the user yet. Review the [guidance](https://docs.microsoft.com/azure/active-directory/manage-apps/application-provisioning-when-will-provisioning-finish-specific-user) for how long provisioning takes as well as the [progress bar](https://docs.microsoft.com/azure/active-directory/manage-apps/application-provisioning-when-will-provisioning-finish-specific-user) on the provisioning configuration page. If the steady state specified in the additional details section is before the date the user was created / updated / deleted, it means we have not evaluated the user yet. In this scenario, the best thing to do is wait for the provisioning service to finish.  

    * Note that our service is only aware of changes to a user in the source system (Cloud HR). There has to be a valid change in the source system for Azure AD to detect the change and flow it into Active Directory.   

* Provisioning service evaluated the user and determined it should not be provisioned:

	* If you've set an attribute based scoping filter, ensure that the user meets the criteria that you have specified
	* If users already exist in the target system and the state of the user in the source and target match, we won't take any further action

* Provisioning service attempted to provision the user and it failed. For these scenarios, review the troubleshooting and recommendations tab of the provisioning logs:

	* A required attribute on the user might be missing in on-premises Active Directory or Azure AD. For example, the userPrincipalName or samAccountName generation rules are not generating the right value.  
    * The matching attribute (usually employeeId) is not resolving to a unique user in on-premises Active Directory or Azure AD. For example, there are two users with the same employeeId in AD and the service returns an error code indicate duplicate target entries for the same source entry. 

## **Recommended Documents**

* [Check the status of the provisioning job to determine if it has completed](https://docs.microsoft.com/azure/active-directory/manage-apps/application-provisioning-when-will-provisioning-finish-specific-user)
* [Review the provisioning logs for an issue with a specific user](https://docs.microsoft.com/azure/active-directory/reports-monitoring/concept-provisioning-logs)
