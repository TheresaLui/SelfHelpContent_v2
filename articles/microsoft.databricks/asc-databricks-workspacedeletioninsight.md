<properties
    pageTitle="Databricks workspace failed to delete"
    description="Unable to delete Databricks workspace."
    infoBubbleText="Unable to delete databricks workspace {Resourcename} due to incorrect managed resource group configured."
    service="microsoft.databricks"
    resource="workspaces"
    authors="nsarang"
    ms.author="nsarang"
    displayOrder=""
    articleId="Databricks_Workspace_Deletion"
    diagnosticScenario="DatabricksWorkSpaceDeletionInsight"
    selfHelpType="rca"
    supportTopicIds="32677666, 32677735, 32677734, 32677737, 32677733"
    resourceTags=""
    productPesIds="16432"
    cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found the following issue
<!--issueDescription-->
Unable to delete databricks workspace <!--$Resourcename-->[Resourcename]<!--/$Resourcename--> due to incorrect managed resource group configured. 
<!--/issueDescription-->

## **Recommended Steps**

1. Login to portal and navigate to databricks workspace <!--$Resourcename-->[Resourcename]<!--/$Resourcename--> 
2. Click on "Managed Resource Group"
3. Click on "Locks" and check if there are any locks on the Managed Resource Group
4. If there are no locks, delete the Managed Resource Group
5. Try deleting workspace by clicking "Delete" button
6. The locks on the above Managed Resource Group need to be removed before the delete can succeed. Please notify Engineering Team to enable 'Bypass Management Locks'.
7. Once enabled, notify customer to delete Managed Resource Group and delete workspace
