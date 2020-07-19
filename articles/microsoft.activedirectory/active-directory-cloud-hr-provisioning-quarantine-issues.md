<properties
	pageTitle="Troubleshooting quarantine issues with Workday provisioning"
	description="Troubleshooting quarantine issues with Workday provisioning"
	infoBubbleText="Troubleshooting quarantine issues with Workday provisioning"
	service="microsoft.activedirectory"
	resource="activedirectory"
	authors="cmmdesai"
	ms.author="chmutali"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32684504"
	productPesIds="16666"
	articleId="8d591007-b405-4b63-9f3e-451f17322ef4"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Troubleshooting quarantine issues with Workday provisioning

## **Recommended Steps**

**Workday to AD User Provisioning goes into quarantine state and no users are created in AD**

The Workday to AD User Provisioning job has gone into quarantine state and the audit logs show export failure events with the error message "Error: OperationsError-SvcErr: An operation error occurred. No superior reference has been configured for the directory service. The directory service is therefore unable to issue referrals to objects outside this forest." This error usually shows up if the Active Directory Container OU is not set correctly or if there are issues with the **Expression Mapping** used for **parentDistinguishedName**.

Check the **Default OU for New Users** parameter for typos. Ensure that the OU specified already exists in your AD. If you are using **parentDistinguishedName** in the attribute mapping ensure that it always evaluates to a known container within the AD domain. Check the **Export event** in the audit logs to see the generated value.

## **Recommended Documents**

* [Tutorial: Configure Workday for automatic user provisioning](https://docs.microsoft.com/azure/active-directory/saas-apps/workday-inbound-tutorial)
