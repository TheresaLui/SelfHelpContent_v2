<properties
	  pageTitle="60 Character limit on Unique Key definition issue"
	  description="60 Character limit on Unique Key definition issue"
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
	  articleId="fd98ff0f-e924-43c1-a072-e55a300974fd"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# 60 Character limit on Unique Key definition issue

<!--issueDescription-->

Dear customer,

The MongoDB unique index spec gets translated to a string, where the max limit is 60 characters. You can calculate the number of allowed characters (or get close to it) with this formula:

Number of total characters allowed in field names in the unique index = 60 - ((number of total path components - 1) * 3) - ((number of property paths) * 5) - (number of dots)

So if you have a unique index of the form:
`
{"a":1, "b":1, "c":1, "d":1, "e":1, "f":1, "g":1}
`

There are 7 path components, 7 property paths, and zero dots.


Number of total characters allowed is 60 - ((7 - 1) * 3) - (7 * 5) - 0 = 7. These 7 are already used, so adding a character to any of the field names above gets the error.

For the customer?s a, b.c, d.e, d.g, there are 7 path components, 4 property paths, and 3 dots, so 60 - ((7 - 1) * 3) - (4 * 5) - 3 = 19, so I would expect they could add 12 more characters to the 7 they already used before hitting the limit.

Prior to the $t/$v Mongo schema, the formula was different and you limit would have been effectively higher, so that could explain why older account works with a unique index that can?t be set on a newer account. You can work around the issue by shortening field names and using fewer/less nested components of your  unique index.

Thank you.

<!--/issueDescription-->

