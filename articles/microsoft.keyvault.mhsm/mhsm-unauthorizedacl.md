<properties
	pageTitle="Key Vault Managed HSM recommendations"
	description="An application does not have sufficient permissions to perform operations on Managed HSM."
	infoBubbleText="Found an issue with Managed HSM access policies"
	service="microsoft.keyvault"
	resource="managedHsms"
	authors="qinx"
	ms.author="qinx"
	displayOrder=""
	articleId="managedhsm-unauthorizedacl"
	diagnosticScenario="managedhsm-recommendations"
	selfHelpType="Diagnostics"
	supportTopicIds="xxxx"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
	ownershipId="AzureKeyVault_MHSM"
/>

# You have Key Vault recommendations

<!--issueDescription-->
An application(s) does not have sufficient permissions to perform operations on '{PoolName}' Managed HSM.
<!--/issueDescription-->

## **Recommended Steps**

We have found in our logs that operation(s) **{ActivityName}** of an application with object id '**{CallerId}**' was denied at around {ActivityTime} UTC between problem start time {ProblemStartTime} UTC and {CaseCreationTime} UTC.   \r\n\r\nMake sure this service principal is the one used in user's application.\r\n  \r\nTo solve this problem, ask an administrator ( a user in Managed HSM builtin roles \"Managed HSM Administor\" ) of Managed HSM '**{PoolName}**' to assign a appropriate role to the application with service principal id '**{CallerId}**'.  \r\n  \r\n  \r\nFor example using Azure CLI, run this command as the administrator of the Managed HSM '{PoolName}':\r\n- To give key encrypt/decrypt operations to the application:\r\n  ```\r\n  az keyvault role assignment create --assignee \"{CallerId}\" --role \"Managed HSM Crypto User\" --scope \"/\" --hsm-name {PoolName}\r\n  ```\r\n\r\n- To give key additional key create/delete operations to the application: \r\n\r\n  ```\r\n  az keyvault role assignment create --assignee \"{CallerId}\" --role \"Managed HSM Crypto Officer\" --scope \"/\" --hsm-name {PoolName}\r\n  ```\r\n\r\nRole \"Managed HSM Administrator\" has all the permissions.\r\n\r\nTo list all the administorators of this Managed HSM, run Azure CLI command:\r\n```\r\naz keyvault role assignment list --hsm-name {PoolName} --role \"Managed HSM Administrator\"\r\n```\r\n\r\nSee links below for details of different builtin roles' permissions in Managed HSM."
    

## **Recommended Documents**

Refer to the following documents to help set up logging and use Azure Monitor. 

* [Managed HSM local RBAC built-in roles](https://docs.microsoft.com/azure/key-vault/managed-hsm/built-in-roles)
* [Managed HSM access control](https://docs.microsoft.com/azure/key-vault/managed-hsm/access-control)
