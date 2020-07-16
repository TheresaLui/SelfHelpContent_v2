<properties
	pageTitle="Troubleshooting provisioning service issues"
	description="Troubleshooting provisioning service issues"
	infoBubbleText="Troubleshooting provisioning service issues"
	service="microsoft.activedirectory"
	resource="activedirectory"
	authors="ArvindHarinder1"
	ms.author="ArvindHarinder1"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32684509"
	productPesIds="16666"
	articleId="4bdf7902-fce3-428b-8587-80fcfd1988fd"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Troubleshooting service issues while provisioning users to an application

If most or all of the calls made against the target system consistently fail due to an error (such as in the case of invalid admin credentials), then the provisioning job goes into a "quarantine" state.

## **Recommended Steps**

* Review the progress bar to understand why the application is in [quarantine](https://docs.microsoft.com/azure/active-directory/app-provisioning/application-provisioning-quarantine-status).

* Review the audit logs and set the activity filter to "Quarantine" to see the quarantine history for the application.

* Review the [provisioning logs](https://docs.microsoft.com/azure/active-directory/reports-monitoring/concept-provisioning-logs) to get detailed error information. 

* Use the [on-demand provisioning](https://docs.microsoft.com/azure/active-directory/app-provisioning/provision-on-demand) capability to provision a user and get detailed diagnostics about the steps taken.


## **Recommended Documents**

* [Learn more about quarantine](https://docs.microsoft.com/azure/active-directory/app-provisioning/application-provisioning-quarantine-status)
* [Reporting on automatic user account provisioning](https://docs.microsoft.com/azure/active-directory/manage-apps/check-status-user-account-provisioning)
* [Problem configuring provisioning to an application](https://docs.microsoft.com/azure/active-directory/manage-apps/application-provisioning-config-problem)
