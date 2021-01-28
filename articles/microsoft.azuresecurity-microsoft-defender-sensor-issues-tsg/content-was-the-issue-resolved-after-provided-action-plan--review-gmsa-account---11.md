<properties
	  pageTitle="Was the issue resolved after provided action plan (review GMSA account)?"
	  description="Was the issue resolved after provided action plan (review GMSA account)?"
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
	  articleId="ffa51d88-b3bc-4d5b-8927-35319c748a0b"
	  ownershipId="Azure_Security_Security_Center"
/>

# Was the issue resolved after provided action plan (review GMSA account)?

If the log indicated the issue: 

~~~powershell

Warn GroupManagedServiceAccountImpersonationHelper GetGroupManagedServiceAccountAccessTokenAsync failed GMSA password could not be retrieved [errorCode=AccessDenied AccountName=account_name DomainDnsName=domain1.test.local]

~~~

This means that the MDI is not able to pull the password related to the GMSA so the customer will need to review the configuration related to this account. Please make sure that the sensor has been granted permission to retrieve the account's credentials. In the applied policy, you may need to add the gMSA account to the Log on as a service user right assignments.

Please refer to the below docs: 

[Getting started with group managed service accounts](https://docs.microsoft.com/windows-server/security/group-managed-service-accounts/getting-started-with-group-managed-service-accounts#BKMK_CreateGMSA)
[How to set up a GMSA account](https://docs.microsoft.com/defender-for-identity/install-step2#how-to-set-up-a-gmsa-account)
