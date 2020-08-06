<properties
	pageTitle="Portal access issues"
	description="Providing users with information about resolving Azure EA Portal access issues"
	infoBubbleText=""
	service="microsoft.enterpriseagreement"
	resource="enrollmentmanagement"
    authors="irinakolontaev1"
	ms.author="baolcsva"
	displayOrder=""
	articleId="72f10d1f-2759-44d5-be8c-ac78ba1b1cd2"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32688688"
	resourceTags=""
	productPesIds="16867"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureEA_SelfDeflectionContent"
/>

# Portal access issues	

The Azure EA portal is used to manage enterprise agreement users and costs. You might encounter these issues when you're configuring or updating Azure EA portal access.

## **Recommended Steps**

### **Issues adding an admin to an enrollment**	

There are different types of authentication levels for enterprise enrollments. When authentication levels are applied incorrectly, you might have issues when you try to sign into the Azure EA portal.	There are different types of authentication levels for enterprise enrollments. When authentication levels are applied incorrectly, you might have issues when you try to sign into the Azure EA portal.

You use the Azure EA portal to grant access to users with different authentication levels. An enterprise administrator can update the authentication level to meet security requirements of their organization.	You use the Azure EA portal to grant access to users with different authentication levels. An enterprise administrator can update the authentication level to meet security requirements of their organization.


### **Authentication level types**

- Microsoft Account Only: For organizations that want to use, create, and manage users through Microsoft accounts <br>
- Work or School Account: For organizations that have set up Active Directory with Federation to the Cloud and all accounts are on a single tenant <br>
- Work or School Account Cross Tenant: For organizations that have set up Active Directory with Federation to the Cloud and will have accounts in multiple tenants <br>	
- Mixed Account: Allows you to add users with Microsoft Account and/or with a Work or School Account <br>

The first work or school account added to the enrollment determines the _default_, or _master_ domain. To add a work or school account with another tenant you must change the authentication level under the enrollment to cross-tenant authentication.

To update the Authentication level:	
1. Sign in to the Azure EA portal as an Enterprise Administrator	
1. Click  **Manage**  on the left navigation panel
1. Click the  **Enrollment**  tab
1. Under **Enrollment Details**, select **Authentication Level**	
1. Click the pencil symbol
1. Click  **Save**

Microsoft accounts must have an associated ID created at [https://signup.live.com](https://signup.live.com).

Work or school accounts are available to organizations that have set up Active Directory with federation and where all accounts are on a single tenant. Users can be added with work or school federated user authentication if the company's internal Active Directory is federated. If your organization doesn't use Active Directory federation, you can't use your work or school email address. Instead, register or create a new email address and register it as a Microsoft account.	

### **Unable to access the Azure EA portal**

If you get an error message when you try to sign into the Azure EA portal, use the following the troubleshooting steps:	


- Ensure that you're using the correct Azure EA portal URL, which is [https://ea.azure.com](https://ea.azure.com) 
- Determine if your access to the Azure EA portal was added as a work or school account or as a Microsoft account: 	

	* If you're using your work account, enter your work email and work password. Your work password is provided by your organization. You can check with your IT department about how to reset the password if you've issues with it.
	* If you're using a Microsoft account, enter your Microsoft account email address and password. If you've forgotten your Microsoft account password, follow the steps on the sign in page to reset the password.
- You should use an in-private or incognito browser session to sign in so that no cookies or cached information from previous or existing sessions are retained. Clear your browser's cache and use an in-private or incognito window to open [https://ea.azure.com](https://ea.azure.com). <br>
- If you get an _Invalid User_ error when using a Microsoft account, it might be because you have multiple Microsoft accounts. The one that you're trying to sign in with isn't the primary email address.
- Or, if you get an _Invalid User_ error, it might be because the wrong account type was used when the user was added to the enrollment. For example, a work or school account instead of a Microsoft account. In this example, you have another EA admin add the correct account or you need to contact.

## **Recommended Documents**

- [Troubleshoot Azure subscription sign-in issues](https://docs.microsoft.com/en-us/azure/billing/billing-troubleshoot-sign-in-issue) <br>
- [Create another enterprise admin](https://docs.microsoft.com/azure/billing/billing-ea-portal-get-started#create-another-enterprise-admin) 
- [What is Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis) 

