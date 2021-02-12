<properties
	pageTitle="I created a review, but the reviewer did not receive an email regarding the required action"
	description="After creating a review, the reviewer doesn't receive an email"
	service="microsoft.aad"
	resource="Microsoft_AAD_ERM"
	authors="kyschaub"
	ms.author="kyschaub"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="governance_overview"
	productPesIds=""
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="958025bf-da79-48d8-99ec-79dc335420d8"
	ownershipId="AzureIdentity_User"
/>

# I created a review, but the reviewer did not receive an email regarding the required action

If the reviewer didn't receive the email, it is possible that his/her email address was not populated correctly in Azure AD. If the reviewer still hasn't received the email, he or she can find all pending access reviews via the MyApps portal.

## **Recommended Steps**

* Ensure that the user's email address is correctly populated in Azure AD:

    * If the user is created in Active Directory and has an Exchange on-premises mailbox, then the administrator should check that the user has a value email address in their 'mail' attribute in Azure AD
    * For internal users who have an Office 365 assigned plan and an Exchange Online mailbox, the administrator should check that the user has a valid email address in their 'mail' attribute
    * For internal users that do not have either Exchange or Exchange Online mailbox, the administrator should check that the user has exactly one value in the 'OtherMails' attribute
    * For external users, the administrator should check that the left hand side of the user's UserPrincipalName (before the "#EXT") can be converted to the user's current email address. If not, then the user should be removed and re-invited with their correct email address.

* Alternatively, sign in to the MyApps portal at [https://myapps.microsoft.com](https://myapps.microsoft.com):

    * In the upper-right corner of the page, click the user symbol, which displays your name and default organization. If more than one organization is listed, select the organization that requested an access review.
    * On the right side of the page, click the Access reviews tile to see a list of the pending reviews. If the tile isn't visible, there are no access reviews to perform for that organization and no action is needed at this time.
    * Click the Begin review link for the access review you want to perform
