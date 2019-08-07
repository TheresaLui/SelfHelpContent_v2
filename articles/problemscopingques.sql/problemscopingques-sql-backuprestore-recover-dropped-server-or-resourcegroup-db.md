<properties
	pageTitle="Recover dropped server or resource group"
	description="Scoping questions to recover-dropped-server-or-resourcegroup"
	authors="andikshi"
	ms.author="andikshi"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630451"
	productPesIds="13491"
	cloudEnvironments="Public"
	schemaVersion="1"
	articleId="problem-scopingques-sql-backuprestore-recover-dropped-server-or-resourcegroup-db"
/>
# Scoping questions to recover-dropped-server-or-resourcegroup
---
{
	"resourceRequired": false,
	"subscriptionRequired": true,
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
                    "value": "ResourceGroup",
                    "text": "ResourceGroup"
                },
                {
                    "value": "Server",
                    "text": "Server"
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
            "visibility": "resource_type_dropdown == ResourceGroup",
            "controlType": "textbox",
            "displayLabel": "What is the resourcegroup that was deleted?",
            "infoBalloonText": "Enter the name of the resourcegroup that was deleted and you want to restore.",
            "required": false
        },
        {
            "id": "target_server_name",
     	    "order": 3,
            "visibility": "resource_type_dropdown == Server",
            "controlType": "textbox",
            "displayLabel": "What is the server or resourcegroup that was deleted?",
            "infoBalloonText": "Enter the name of the server that was deleted and you want to restore.",
            "required": false
        },
	{
            "id": "target_server_resourcegroup_name",
     	    "order": 4,
            "visibility": "resource_type_dropdown == dont_know_answer",
            "controlType": "textbox",
            "displayLabel": "What is the server or resourcegroup that was deleted?",
            "infoBalloonText": "Enter the name of the server or resourcegroup that was deleted and you want to restore.",
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
            "watermarkText": "Please provide additional context about how the resource was deleted, Business justification for restore , any other specifications."
        }
    ],
    "$schema": "SelfHelpContent"
}
---
