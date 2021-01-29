<properties
	  pageTitle="Sparse Unique Key Support issue"
	  description="Sparse Unique Key Support issue"
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
	  articleId="fb481684-8491-46fe-9354-e65e338b0687"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Sparse Unique Key Support issue

<!--issueDescription-->

Dear customer,

**Summary:**
You are inserting or creating a document with null values for the Unique key Properties. The insert would fail with "duplicate key error collection" if multiple document are passed with null.

**Example:**
Unique Key on FirstName and LastName Property
```
{
   'firstName' : 'My first name',
   'lastName': 'My lastName',
}
```
The null is passed if the document does not have any property defined and would lead to Duplicate Key Error

**Mitigation:**
The workaround is to pass a unique non meaningful values for Unique Properties. You can use GUID to avoid the duplicate error.

Thank you.

<!--/issueDescription-->

