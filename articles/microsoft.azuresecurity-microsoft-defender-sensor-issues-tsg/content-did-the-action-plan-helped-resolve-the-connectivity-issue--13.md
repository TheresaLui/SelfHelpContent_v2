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

Check Sensor and updater logs, this issue can be caused by a Firewall block or a timeout. If the log shows:

~~~Powershell

System.Net.Http.HttpRequestException: An error occurred while sending the request. ---> System.Net.WebException: Unable to connect to the remote server ---> System.Net.Sockets.SocketException: A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond

~~~

This error points to a failure of communication with the MDI portal. We should advise the customer to ensure that all the pre-requisites ports are allowed and ensure that communication is allowed in firewall and proxy. .

If the log shows: 

~~~powershell

Error DirectoryServicesClient Microsoft.Tri.Infrastructure.ExtendedException: Failed to communicate with configured domain controllers at new Microsoft.Tri.Sensor.DirectoryServicesClient(IConfigurationManager configurationManager, IDomainNetworkCredentialsManager

~~~

And a health alert is generated in the MDI Portal:

~~~powershell

Directory services user credentials are incorrect
Credentials for the directory services user contoso\AATP are incorrect. Your MDI sensor(s) cannot connect to
contosodc1.contoso.com
without these credentials. The directory services user is required to perform LDAP queries against the domain controllers.

~~~

These issue point to account password issues, it is recommended to advise the customer to double check the credentials configured in the MDI portal.

Please refer to the below docs: 

[Defender for identity pre-requisite ports](https://docs.microsoft.com/defender-for-identity/prerequisites#ports)

