<properties
	  pageTitle="Query Top Consuming Rus issue"
	  description="Query Top Consuming Rus issue"
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
	  articleId="bf6b8eda-caf6-4052-bdef-a6dbb3e65969"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Query Top Consuming Rus issue

<!--issueDescription-->

Dear customer,

We have Category named ?QueryRuntimeStatistics? in the Cosmos DB Diagnostics logging which would log the Query Text in obfuscated form.  This would help you to identify the structure of the query which is driving the RU. The Query Text and the RU charges are logged as two individual events with same activity ID. You can use the Activity ID to list the query and the associated RU cost of a given query.

The logging of Query Text can be made it to be Plain Text through a custom configuration.  This require engaging the PG team for this configuration.  Logging in plain text would expose a security issue for many customer since any user who has Monitoring role can review the query.  At this time,  this option is not available to all customer.  However, this can be enable on need basis after explaining the implication.

See [example](https://microsofteur-my.sharepoint.com/:i:/g/personal/anferrei_microsoft_com/EUfX4QUuyvFFpnP83dtAMrABEdZgZiis8Egef8IvIzV5Wg?e=mvMVZa)

## Important Notes
- As of now, this is only for ?SQL QUERY?.
- The Storage procedure has the procedure code and the query.  The query part would be still logged.

Thank you.

<!--/issueDescription-->

