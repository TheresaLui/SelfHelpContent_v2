<properties
	pageTitle="Troubleshooting Workday provisioning service issues"
	description="Troubleshooting Workday provisioning service issues"
	infoBubbleText="Troubleshooting Workday provisioning service issues"
	service="microsoft.activedirectory"
	resource="activedirectory"
	authors="cmmdesai"
	ms.author="chmutali"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32684523"
	productPesIds="16666"
	articleId="8d591007-b407-4b63-9f3e-451f17322ef4"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Troubleshooting Workday provisioning service issues

## **Recommended Steps**

**Workday to AD User Provisioning goes into quarantine state over weekends**

The Workday to AD User Provisioning job goes into quarantine state over the weekends (Fri-Sat) and we get an email notification that there is an error with the synchronization.

One of the common causes for this error is the planned Workday downtime. If you are using a Workday implementation tenant, please note that Workday has scheduled down time for its implementation tenants over weekends (usually from Friday evening to Saturday morning) and during that period the Workday provisioning apps may go into quarantine state as it is not able to connect to Workday. It gets back to normal state once the Workday implementation tenant is back online. In rare cases, you may also see this error, if the password of the Integration System User changed due to tenant refresh or if the account is in locked or expired state.

Check with your Workday administrator or integration partner to see when Workday schedules downtime to ignore alert messages during the downtime period and confirm availability once Workday instance is back online.

## **Recommended Documents**

* [Tutorial: Configure Workday for automatic user provisioning](https://docs.microsoft.com/azure/active-directory/saas-apps/workday-inbound-tutorial)
