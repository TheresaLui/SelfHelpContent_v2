<properties
	  pageTitle="Isolate the issue to see if it is related to AAD Auth or Storage Firewall. "
	  description="Isolate the issue to see if it is related to AAD Auth or Storage Firewall. "
      service="Microsoft.Storage"
      resource="Microsoft.Storage/storageAccounts,Microsoft.ClassicStorage/storageAccounts"
	  authors="yagohel23"
	  ms.author="yagohel"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds="32679285,32679299,32679292,32678715"
	  resourceTags=""
	  productPesIds="16459,16461,15629,16598"
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="e5db88db-f01e-48bd-8f35-286a0f7e74ed"
	  ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Isolate the issue to see if it is related to AAD Auth or Storage Firewall. 

Anytime a particular user is not able to access data in Storage Account, they will get an **Unauthorized** error. This error can happen due to multiple reason like not having AAD permission, firewall blocking the request or the SAS token being invalid. Before you consider customer's issue to be an AAD issue, make sure you verify the failure is actually due to customers not having appropriate AAD permissions. 

Engineers should review the Insights in ASC. Insights on these topics are pretty accurate and will give a general idea of the issue the customer could be facing. 

This can also easily be verified by looking at the Dgrep logs in Jarvis. Run a Dgrep query similar to the following on the customer's storage account for the period during which they reported an issue and see the InternalStatus column of each 403 failure in there. [https://jarvis-west.dc.ad.msft.net/48FAFDC2](https://jarvis-west.dc.ad.msft.net/48FAFDC2)(Replace Anyfield filter with customer's storage account and change the tenant filter as well accordingly.Also, dont forget to change the timeframe for this query.)

While using dgrep, check the case details to see if the customer has provided a storage server request id. Plug that into dgrep to get to the right failure.

Once you know the InternalStatus of the failure, use the table below to determine if your customer's issue is related to AAD Auth, Firewall or SAS Tokens.

| Internal Status                                                                   | Root Cause       |
|-----------------------------------------------------------------------------------|------------------|
| OAuthAuthorizationError                                                           | AAD Auth failure |
| OAuthIpAuthorizationError or SASIpAuthorizationError(Anything which has IP in it)&nbsp;&nbsp;&nbsp;&nbsp; | Firewall failure |
| SASAuthorizationError                                                             | SAS failure      |

You can also use the AuthenticationType column in Dgrep to determine if the request was made over AAD or SAS. Before moving forward with this TSG, it is important that we first verify whether the issue is with AAD, Firewall or SAS. 

While using dgrep, check the case details to see if the customer has provided a storage server request id. Plug that into dgrep to get to the right failure.

Sometimes you may also see the internal status as "AuthenticationError" for a 403 failure. If the Status field shows the following error, this is usually caused by the customer connecting using a an incorrect Storage account key. Please ask them to update the storage account key in their application with the most recent storage account key. This can be grabbed from the portal.

**Server failed to authenticate the request. Make sure the value of Authorization header is formed correctly including the signature.**

