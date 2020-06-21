<properties
	  pageTitle="TSG Content Step: Check whether the backend pool is empty"
	  description="TSG Content Step:Check whether the backend pool is empty"
	  service="microsoft.network"
	  resource="applicationGateway"
	  authors="JRMayberry"
	  ms.author="rimayber"
	  displayOrder=""
	  selfHelpType="TSG_Content"
          supportTopicIds=""
          resourceTags=""
          productPesIds=""
          cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="f1b32390-c392-4dd1-9455-1e28a3710193"
	ownershipId="CloudNet_AzureApplicationGateway"
/>


# How to check if the backend pool is empty:

1. In ASC Resource Explorer, for the Application Gateway in question, check the listener the customer is trying to access using the domain name. You can find the domain name the customer is using from the scoping question in the case details. If the customer doesn't have any multi-site listeners, then it should match with the basic listener. If domain name and URL are not mentioned, reach out to the customer.
2. Check the request routing rule to which the listener is associated with
3. Note the name of the backend pool associated to the listener
4. Navigate to the **Backend Address Pools** section and check the appropriate backend pool configuration
5. If both the backend IP address/FQDN and backend IP configuration shows N/A, then it is empty
