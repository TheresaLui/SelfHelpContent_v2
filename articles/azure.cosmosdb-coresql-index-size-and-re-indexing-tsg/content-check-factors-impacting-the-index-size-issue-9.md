<properties
	  pageTitle="Check Factors impacting the Index Size issue"
	  description="Check Factors impacting the Index Size issue"
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
	  articleId="c60b255a-4ec1-452f-b6aa-8f33ddc2abde"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Check Factors impacting the Index Size issue

1. The index size is based on the Index Definition. In other words, indexing all properties would have large size then the specified properties
2. The Index space is compacted on continuous basis by the Service.  However, the compaction does not run against the indexes which are less than 150 MB. In other words, the index spaces would not be released after any data deletion for space less than 150MB.
3. The Index size can grow or double on the below cases
   1. Partition Split duration. The space would be released after the split is completed.
   2. Index V1 to Index V2. The index V2 have changed to handle many query scenarios for which we have to index and keep more meta data which increase the size of the index.  So, the first thing to check is that the Index version was changed for a given collection if the size have not released back.
4. Ensure the Compaction process to release the space back.  PLease note that the compaction process does not have any end  or target to wait.  The goal is to check the process is running, if so then the space is continuously being managed.

