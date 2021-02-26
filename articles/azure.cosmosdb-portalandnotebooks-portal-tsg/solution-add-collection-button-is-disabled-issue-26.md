<properties
	  pageTitle="Add Collection Button is disabled issue"
	  description="Add Collection Button is disabled issue"
      service="Microsoft.DocumentDB"
      resource="databaseAccounts"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="186c87ce-bf9a-446c-bc0e-068a7f32df8e"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Add Collection Button is disabled issue

<!--issueDescription-->

Dear customer,

On the Database blade, the **Add Collection** button is disabled.

#### Solution:
- In the Azure portal, in the Jumpbar, click **Browse**, click **Subscriptions**, click the subscription associated with the DocumentDB database, and then in the **Subscription** blade, click **Manage**. 
- In the new browser window, you'll see that you have no credits remaining. Click the **Remove spending limit** button to remove the spending for only the current billing period or indefinitely. Then complete the wizard to add or confirm your credit card information. 

#### Explanation:
If your Azure subscription is associated with benefit credits, such as free credits offered from an MSDN subscription, and you have used all of your credits for the month, you are unable to create any additional collections in Cosmos DB.

Thank you.

<!--/issueDescription-->

