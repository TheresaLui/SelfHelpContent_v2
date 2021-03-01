<properties
	pageTitle="Key Vault Managed HSM recommendations"
	description="An application does not have sufficient permissions to perform operations on Managed HSM."
	infoBubbleText="Found an issue with Managed HSM access policies"
	service="microsoft.keyvault"
	resource="managedHsms"
	authors="qinx"
	ms.author="qinx"
	displayOrder=""
	articleId="mhsm-unauthorizedacl"
	diagnosticScenario="ManagedHsmUnauthorizedAclInsight"
	selfHelpType="Diagnostics"
	supportTopicIds="xxxx"
	resourceTags=""
	productPesIds="17075"
	cloudEnvironments="public"
	ownershipId="AzureKeyVault_MHSM"
/>

# You have Key Vault Managed HSM recommendations

<!--issueDescription-->
An application(s) does not have sufficient permissions to perform operations on '<!--$PoolName-->[PoolName]<!--/$PoolName-->' Managed HSM.
<!--/issueDescription-->

## **Recommended Steps**

We have run a diagnostics in our logs and identified that operation **<!--ActivityName-->[ActivityName]<!--/ActivityName-->** of an application with service principal id '**<!--CallerId-->[CallerId]<!--/CallerId-->**' was denied at around <!--ActivityTime-->[ActivityTime]<!--/ActivityTime--> UTC between problem start time <!--ProblemStartTime-->[ProblemStartTime]<!--/ProblemStartTime--> UTC and <!--CaseCreationTime-->[CaseCreationTime]<!--/CaseCreationTime--> UTC.   

To solve this problem, 

1. Make sure this service principal is the one used in your application. 

2. Ask an administrator ( a user in Managed HSM builtin roles \"Managed HSM Administor\" ) of Managed HSM '**<!--PoolName-->[PoolName]<!--/PoolName-->**' to assign a appropriate role to the application with service principal id '**<!--CallerId-->[CallerId]<!--/CallerId-->**'.
 
  For example when using Azure CLI, run this command as the administrator of the Managed HSM '<!--PoolName-->[PoolName]<!--/PoolName-->':
  - To give key encrypt/decrypt operations to the application:
    ```
    az keyvault role assignment create --assignee \"<!--CallerId-->[CallerId]<!--/CallerId-->\" --role \"Managed HSM Crypto User\" --scope \"/\" --hsm-name <!--PoolName-->[PoolName]<!--/PoolName-->
    ```

  - To give key additional key create/delete operations to the application: 

    ```
    az keyvault role assignment create --assignee \"<!--CallerId-->[CallerId]<!--/CallerId-->\" --role \"Managed HSM Crypto Officer\" --scope \"/\" --hsm-name <!--PoolName-->[PoolName]<!--/PoolName-->
    ```

  Role \"Managed HSM Administrator\" has all the permissions.

  To list all the administorators of this Managed HSM, run Azure CLI command:
  ```
  az keyvault role assignment list --hsm-name <!--PoolName-->[PoolName]<!--/PoolName--> --role \"Managed HSM Administrator\"
  ```

  See links below for details of different builtin roles' permissions in Managed HSM.

## **Recommended Documents**

Refer to the following documents to setup permissions for your application.

* [Managed HSM local RBAC built-in roles](https://docs.microsoft.com/azure/key-vault/managed-hsm/built-in-roles)
* [Managed HSM access control](https://docs.microsoft.com/azure/key-vault/managed-hsm/access-control)
