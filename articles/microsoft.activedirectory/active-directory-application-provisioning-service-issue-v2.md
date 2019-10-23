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
	cloudEnvironments="Public"
/>

# Troubleshooting service issues while provisioning users to an application

If most or all of the calls made against the target system consistently fail due to an error (such as in the case of invalid admin credentials), then the provisioning job goes into a "quarantine" state.

## **Recommended Steps**

* Review the provisioning summary report at the bottom of the provisioning configuration page

* Review provisioning errors in the Azure AD audit logs. From there you can get detailed information about which users were unsuccessfully provisioned, as well as details about the error. 

## **Recommended Documents**

* [Reporting on automatic user account provisioning](https://docs.microsoft.com/azure/active-directory/manage-apps/check-status-user-account-provisioning)
* [Problem configuring provisioning to an application](https://docs.microsoft.com/azure/active-directory/manage-apps/application-provisioning-config-problem)