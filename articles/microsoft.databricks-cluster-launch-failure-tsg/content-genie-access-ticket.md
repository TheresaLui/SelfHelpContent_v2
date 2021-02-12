<properties pageTitle="Check if a genie access ticket has been created"
            description="Check if a genie access ticket has been created"
            service="Microsoft.Databricks"
            resource="Microsoft.Databricks/workspaces"
            authors="JRMayberry"
            ms.author="rimayber"
            displayOrder=""
            selfHelpType="TSG_Content"
            supportTopicIds=""
            resourceTags=""
            productPesIds=""
            cloudEnvironments="public, fairfax, usnat, ussec"
            articleId="f6ffb617-de71-4ba5-85eb-9872cff960d1"
            ownershipId="Centennial_CloudNet_LoadBalancer" />

# Check if a genie access ticket has been created

Genie tool is an application that with customer permission allows CSS to access:

1.	Customers workspace
2.	Databricks control plane logs
3.	Customers spark logs

Check in the case that the **DatabricksConsent**  is **True**. This gives Microsoft and Databricks permissions to access customers workspace and logs.

**Important**: If DatabricksConsent is False, please get customer written or verbal consent before accessing Genie.
