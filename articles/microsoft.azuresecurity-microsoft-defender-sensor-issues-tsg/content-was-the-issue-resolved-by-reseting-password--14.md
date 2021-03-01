<properties
	  pageTitle="Was the issue resolved by reseting password?"
	  description="Was the issue resolved by reseting password?"
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
	  articleId="192e9ab8-cb20-4d2e-90cf-9ea20fbe8ba7"
	  ownershipId="Azure_Security_Security_Center"
/>

# Was the issue resolved by reseting password?

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

These issue point to account password issues, it is recommended to advise the customer to double check the credentials configured in the MDI portal. If they don't recall or forgot your password you need to reset the account password and then update the password on the MDI portal in the directory tab
