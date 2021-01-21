<properties
	  pageTitle="MongoDB wire version issues"
	  description="MongoDB wire version issues"
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
	  articleId="7499039e-ff05-4e7d-8bb3-dfbf32c043a0"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# MongoDB wire version issues

<!--issueDescription-->

Dear customer,

Some versions of MongoDB drivers require the initial handshake include a minimum wire protocol version.  
* Accounts on server version 3.6, the drivers should work with no change required   
* Accounts on server version 3.2, if the driver throws an error related to the wire protocol version, try enabling the preview feature for wire protocol version 3.4 and appending an appName identifying the account to the connection string: &appName=@accountName@ 

Thank you.

<!--/issueDescription-->

