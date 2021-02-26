<properties
	  pageTitle="Legacy geospatial commands not yet supported issue"
	  description="Legacy geospatial commands not yet supported issue"
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
	  articleId="cfaf77a7-ccf5-4d24-a5c0-04ed528bb9fb"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Legacy geospatial commands not yet supported issue

<!--issueDescription-->

Dear customer,

The command db.geo2dcoll.find({ 'position': { '$geoWithin': {'$center': [ [0, 0],2]}}}) returns the error:

#### Error
```
Legacy geospatial commands not yet supported, 
code: 115,
codeName: CommandNotSupported
```

#### Solution: 
Please switch to using $geometry instead of $center

#### Documentation: 
- https://docs.microsoft.com/en-us/azure/cosmos-db/mongodb-feature-support-36#geospatial-operators

Thank you.

<!--/issueDescription-->

