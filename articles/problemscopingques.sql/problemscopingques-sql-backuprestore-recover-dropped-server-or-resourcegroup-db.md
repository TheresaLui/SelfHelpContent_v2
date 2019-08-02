<properties
	pageTitle="Recover-dropped-server-or-resourcegroup"
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
	"resourceRequired": true,
	"subscriptionRequired": true,
    "formElements": [
        {
            "id": "target_server_resource_group",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "What is the server or resourcegroup that was deleted?",
            "infoBalloonText": "Enter the server or resourcegroup that was deleted and you want to restore.",
            "required": false
        },
	{
            "id": "problem_start_time",
            "order": 2,
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
