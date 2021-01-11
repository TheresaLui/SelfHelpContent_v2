<properties
	  pageTitle="Did the action plan helped resolve the connectivity issue?"
	  description="Did the action plan helped resolve the connectivity issue?"
      service="Microsoft.Security"
      resource="Microsoft.Security/assessments"
	  authors="rimayber"
	  ms.author="rimayber"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="53fc686c-7262-407a-9cd6-165073477508"
	  ownershipId="Azure_Security_Security_Center"
/>

# Did the action plan helped resolve the connectivity issue?

If the log shows: 

~~~Powershell

System.Net.Http.HttpRequestException: An error occurred while sending the request. ---> System.Net.WebException: Unable to connect to the remote server ---> System.Net.Sockets.SocketException: A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond

~~~

This error points to a failure of communication with the MDI portal. We should advise the customer to ensure that all the pre-requisites ports are allowed and insure that communication is allowed in firewall and proxy. 

Please refer to the below docs: 

[Defender for identity pre-requisite ports](https://docs.microsoft.com/defender-for-identity/prerequisites#ports)


