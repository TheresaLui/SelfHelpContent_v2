<properties
pageTitle="This company has exceeded the number of objects that can be synchronized"
	description="This company has exceeded the number of objects that can be synchronized"
	infoBubbleText="This company has exceeded the number of objects that can be synchronized"
	service="microsoft.aad.iam"
	resource="aadconnect"
	authors="rodejo"
	ms.author="rodejo"
	displayOrder="1"
	articleId="ADtoAADSync_AADConnect_ASC_AAD_Connect_Health_Alerts_Exceeded_Quota_Limit"
	diagnosticScenario=""
	selfHelpType="Diagnostics"
	resourceTags=""
	productPesIds="16666"
  cloudEnvironments="public, Fairfax, Mooncake, ussec, usnat"
  ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# This company has exceeded the number of objects that can be synchronized
<!--issueDescription-->
You receive an email message from MSOnlineServicesTeam@MicrosoftOnline.com that contains the following error message:

>Synchronization has been stopped. This company has exceeded the number of objects that can be synchronized. Contact Microsoft Online Services Support.
<!--/issueDescription-->

## **Recommended Steps**

### **Cause**

This issue occurs because the number of objects that you created in your Azure AD exceed your directory service limit. Azure AD limits how many objects can be created by each organization. Groups, contacts, and user objects in your Azure AD organization are counted as part of your organization's directory usage.

Your default directory service quota is calculated according to the following guidelines:

* If you don't have any verified domains, the current directory service quota in Azure AD is 50,000 objects, but:

	* If your organization was created before October 5, 2011, your default directory service quota is 10,000 objects
	* If your organization was created after October 5, 2011 and before May 2012, your default directory service quota is 20,000 objects
	* If your organization was created after May 2012, your default directory service quota is 50,000 objects
	
* If you have at least one verified domain, the default directory service quota in Azure AD is 300,000 objects

### **Solution**

When the number of groups, contacts, and user objects in your on-premises Active Directory exceed your directory service quota, you can request an increase to the directory service quota limitation for your company. This increase lets you sync more objects than the current default limit when you use directory synchronization.

To continue to create objects in your organization, you must either add a domain or request an increase to your directory service quota. To do this, use the following methods.

**Method 1: If you don't have a verified domain**

You must add a domain to increase your quota limit to 300,000 objects. For more information, see [how to add your domain](http://technet.microsoft.com/en-us/library/hh969247.aspx).

**Method 2: If you have more than 300,000 objects in your on-premises Active Directory directory service**

To increase the number of objects that can be synced beyond 300,000, contact Support.

### **More information**

A directory service quota is implemented by using the cloud service as a method to limit the maximum number of objects that can be created and owned by a single security principal. All objects that are synced by using directory synchronization to a company have the creator/owner value set to the default admins group for that company. For example, the admins group is set as *admins@contoso1.microsoftonline.com*. Therefore, this configuration prevents users from creating an unlimited number of objects by using directory synchronization. If a company has a legitimate need to sync more than the directory service quota limit, submit a service request to technical support.

**Frequently asked questions**

Q1. Do objects that were manually added through the cloud service portal or through the cloud service API, such as Exchange Online PowerShell, count against my online company quota?

A1. Yes.

Q2. Do deleted objects count against my online company quota?

A2. Yes. When a cloud service customer deletes an object from an online company, the deleted object is put into a deleted objects container in the  directory service. The object remains in the deleted objects container until the tombstone lifetime expires. The expiration is currently set to 30 days.

For example, consider the following scenario. An online company is evaluating a cloud service by using a nonproduction on-premises Active Directory environment. The cloud service organization was created before October 5, 2011, and the default sync limit is 10,000 objects. The company performs a bulk sync of 8,000 group objects and contact objects by using the Directory Sync tool. Later, the online company decides to do the following:

1. Delete those group objects and contact objects from the company's on-premises nonproduction Active Directory DS environment
2. Add 8,000 user objects to its on-premises nonproduction Active Directory DS environment
3. Sync the updates to its online company

The 8,000 group objects and contact objects are moved to the deleted objects container in the directory service. And these objects continue to consume up to 25 percent of the online company quota until they are permanently removed after the 30-day tombstone period. (This percentage is equal to 2,000 objects, or 8,000 × 25 percent.) Therefore, after syncing the 5,000 new user objects, the online company will consume 10,000 objects of its available Active Directory quota, 2,000 from deleted objects plus 8,000 from new user objects. During the 30-day tombstone period (and this period may coincide with the online company evaluation period), the online company may be unable to add any additional objects by using directory synchronization. This condition occurs because the online company's directory service quota has been reached.

In this scenario, the online company that's performing the evaluation of the cloud service must reduce the number of objects in its nonproduction on-premises Active Directory DS environment to complete the product evaluation. However, if the online company can't reduce the number of objects, the company must request an increase in its directory service quota.

Q3. Does having more than one verified domain mean that I can have a quota that's higher than 300,000 objects?

A3. No. You're granted a directory quota of 300,000 objects if you have one or more verified domains. You're not granted a quota of 300,000 objects for each verified domain that you register.
