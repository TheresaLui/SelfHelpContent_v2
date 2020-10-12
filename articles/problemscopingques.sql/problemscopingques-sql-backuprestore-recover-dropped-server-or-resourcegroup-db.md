<properties
	pageTitle="Recover dropped server or resource group"
	description="Scoping questions to recover-dropped-server-or-resourcegroup"
	authors="andikshi"
	ms.author="andikshi"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630451"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="problem-scopingques-sql-backuprestore-recover-dropped-server-or-resourcegroup-db"
	ownershipId="AzureData_AzureSQLDB_BackupRestore"
/>
# Scoping questions to recover-dropped-server-or-resourcegroup
---
{
	"$schema": "SelfHelpContent",
	"resourceRequired": false,
	"subscriptionRequired": false,
	"formElements": [
	{
            "id": "resource_type_dropdown",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Do you want to restore a resourcegroup or server",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Select from the following",
			"dropdownOptions": [
                {
                    "value": "resource group",
                    "text": "resource group"
                },
                {
                    "value": "server",
                    "text": "server"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Dont know answer"
                }
            ],
            "required": true
        },
	{
            "id": "target_resourcegroup_name",
     	    "order": 2,
            "visibility": "resource_type_dropdown == resource group",
            "controlType": "textbox",
            "displayLabel": "What is the resource group that was deleted?",
            "infoBalloonText": "Enter the name of the resource group that was deleted and you want to restore.",
            "required": false
        },
        {
            "id": "target_server_name",
     	    "order": 3,
            "visibility": "resource_type_dropdown == server",
            "controlType": "textbox",
            "displayLabel": "What is the server that was deleted?",
            "infoBalloonText": "Enter the name of the server that was deleted and you want to restore.",
            "required": false
        },
	{
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When was this deleted?",
            "infoBalloonText": "Enter the approximate time when this was deleted.",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional context for the restore",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Please provide additional context about how the resource was deleted, business justification for restore , and any other specifications if needed."
        }
    ]
}
---
