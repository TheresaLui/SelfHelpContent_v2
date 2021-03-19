<properties
	pageTitle="Cosmos DB Managed Identities scoping questions"
	description="Cosmos DB Managed Identities scoping questions"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="problemScopingQuestions" 
	supportTopicIds="32783450"
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="e4994bc3-9664-4f46-b773-a16bed4d7e78"
	ownershipId="AzureData_AzureCosmosDB"
/>
# CosmosDB Managed Identities Issues
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Cosmos DB Managed Identities Issues",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "database_name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Database name",
            "required": false
        },
        {
            "id": "mgtidentity_using_access_policy",
            "order": 3,
            "controlType": "radioButtonGroup",
            "displayLabel": "Are you using the managed identity of your Azure Cosmos DB account in the access policy of your Azure Key Vault instance?",
            "radioButtonOptions":[
            {
               "value":"Yes",
               "text":"Yes"
            },
            {
               "value":"No",
               "text":"No"
            },
            {
               "value":"dont_know",
               "text":"Don't know"
            }
         ],
            "required": false
        },
        {
            "id": "mgtidentity_key_identifier",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What is the key identifier of the customer-managed key you're using on your Azure Cosmos DB account?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details about the issue that you are facing",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "More information on the exact issue."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
