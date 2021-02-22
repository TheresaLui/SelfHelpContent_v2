<properties
  pagetitle="V2 Data Factory - Cannot Publish Changes"
  service=""
  resource=""
  ms.author="hecepeda,vimals,haoc"
  selfhelptype="Generic"
  supporttopicids="32629446"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="datafactory-v2-authoring-development-issues-cannot-publish.md"
  ownershipid="AzureData_DataFactory" />
# V2 Data Factory - Cannot Publish Changes

## **Recommended Steps**

* To publish changes to the data factory or to create and manage child resources in the Azure portal you must belong to the **Data Factory Contributor** role at the **Resource Group** level or above. Refer to the following articles for more details: [Roles and requirements](https://docs.microsoft.com/azure/data-factory/concepts-roles-permissions#roles-and-requirements) and
[Roles and Permissions](https://docs.microsoft.com/azure/role-based-access-control/role-assignments-portal).

### Common Errors

* **Error: "Unable to publish because the resource group or the Factory contains a lock."**
   This error is due to the [delete lock](https://docs.microsoft.com/azure/azure-resource-manager/management/lock-resources) placed on the Resource Group. To resolve this error, delete the lock on the Resource Group and then publish changes to the data factory. You may reapply the lock after the changes are published successfully. <br>

* **Error: "Failed to save the ARM template in Git since it's size exceeds "xx MB". Please use linked templates instead if you need to do CI/CD integration."** 
   This error is due to ARM template size exceeding 4MB. See how to use [Linked Resource Manager Template](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#linked-resource-manager-templates) feature to break down the entire factory payload into several files so that you aren't constrained by the limits.


- **Error: "InvalidResourceIdentityPrincipalId"**: The Data Factory does not contain a managed identity. This could be caused by moving resources across tenants. <br>

   If you see this error after performing a change on your data factory, you can try generating a new managed identity to resolve it. You can use PowerShell or the REST API as mentioned in [_Generate service identity_](https://docs.microsoft.com/azure/data-factory/data-factory-service-identity#generate-service-identity). To use PowerShell, see the following: <br>

   * **Install PowerShell AZ module, connect to Azure, and select the subscription hosting your Data Factory**: 

      ```
      Install-Module -Name Az -AllowClobber
      Connect-AzAccount
      Get-AzSubscription -SubscriptionName "MyProdSubscription"
      Select-AzSubscription -SubscriptionName "your subscription name" 
      ```

   * **Execute `cmdlet` to create a new managed identity**: 

      ```
      PS C:\WINDOWS\system32> Set-AzDataFactoryV2 -ResourceGroupName <resourceGroupName> -Name <dataFactoryName> -Location <region>
   
      DataFactoryName   : ADFV2DemoFactory
      DataFactoryId     : /subscriptions/<subsID>/resourceGroups/<resourceGroupName>/providers/Microsoft.DataFactory/factories/ADFV2DemoFactory
      ResourceGroupName : <resourceGroupName>
      Location          : East US
      Tags              : {}
      Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
      ProvisioningState : Succeeded
      ```
<br>



## **Recommended Documents**

- How to: [Troubleshoot Git Integration](https://docs.microsoft.com/azure/data-factory/source-control#troubleshooting-git-integration) <br>

**FAQ**

- [ADF FAQ](https://docs.microsoft.com/azure/data-factory/frequently-asked-questions) <br>
- [Feature Request](https://feedback.azure.com/forums/270578-azure-data-factory) <br>
