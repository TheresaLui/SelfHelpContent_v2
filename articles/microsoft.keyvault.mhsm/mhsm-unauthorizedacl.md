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
	supportTopicIds="32736890,32736892,32736893,32736894,32736897,32736900,32736907"
	resourceTags=""
	productPesIds="17075"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureKeyVault_MHSM"
/>

# You have Key Vault Managed HSM recommendations

<!--issueDescription-->
An application does not have sufficient permissions to perform operations on <!--$PoolName-->[PoolName]<!--/$PoolName--> Managed HSM.
<!--/issueDescription-->

## **Recommended Steps**

We have run a diagnostics in our logs and identified that operation **<!--$ActivityName-->[ActivityName]<!--/$ActivityName-->** of an application with service principal id **<!--$CallerId-->[CallerId]<!--/$CallerId-->** was denied at around <!--$ActivityTime-->[ActivityTime]<!--/$ActivityTime--> UTC between problem start time <!--$ProblemStartTime-->[ProblemStartTime]<!--/$ProblemStartTime--> UTC and <!--$CaseCreationTime-->[CaseCreationTime]<!--/$CaseCreationTime--> UTC.   

To resolve this issue: 

1. Make sure that this service principal is the one used in your application. The CLI command below shows the information about this service principal:

  ```
  az ad sp show --id "<!--$CallerId-->[CallerId]<!--/$CallerId-->" 
  ```

2. If this is the right application, ask an administrator (a user in the Managed HSM built-in role, Managed HSM Administor) of Managed HSM **<!--$PoolName-->[PoolName]<!--/$PoolName-->** to assign a appropriate role to service principal id **<!--$CallerId-->[CallerId]<!--/$CallerId-->**, as the following example:<br>
 
 For example, in Azure CLI, run the following command as the administrator of the Managed HSM `<!--$PoolName-->[PoolName]<!--/$PoolName-->`:<br>
 - To give key encrypt/decrypt operations to the application:
  
   ```
    az keyvault role assignment create --assignee "<!--$CallerId-->[CallerId]<!--/$CallerId-->" --role "Managed HSM Crypto User" --scope "/" --hsm-name <!--$PoolName-->[PoolName]<!--/$PoolName-->
    ```

 - To give additional key create/delete operations to the application: 

    ```
    az keyvault role assignment create --assignee "<!--$CallerId-->[CallerId]<!--/$CallerId-->" --role "Managed HSM Crypto Officer" --scope "/" --hsm-name <!--$PoolName-->[PoolName]<!--/$PoolName-->
    ```

 The Managed HSM Administrator role has all the required permissions.

  To list all the administrators of this Managed HSM, run Azure CLI command:
  
  ```
  az keyvault role assignment list --hsm-name <!--$PoolName-->[PoolName]<!--/$PoolName--> --role "Managed HSM Administrator"
  ```

See the following links for more information about different built-in roles' permissions in Azure Managed HSM service.

## **Recommended Documents**

To set up permissions for your application, see the following documents:<br>

* [Managed HSM local RBAC built-in roles](https://docs.microsoft.com/azure/key-vault/managed-hsm/built-in-roles)
* [Managed HSM access control](https://docs.microsoft.com/azure/key-vault/managed-hsm/access-control)
