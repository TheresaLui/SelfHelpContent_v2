<properties
	pageTitle="Geo-restore"
	description="Scoping questions to capture more details about errors\issues encountered while trying to Geo-restore SQL DB"
	authors="andikshi"
	ms.author="andikshi"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630425"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake"
	schemaVersion="1"
	articleId="problem-scopingques-sql-backuprestore-georestore-db"
	ownershipId="AzureData_AzureSQLDB"
/>
# Error when trying to geo-restore
---
{
	"$schema": "SelfHelpContent",
	"resourceRequired": false,
	"subscriptionRequired": false,
	"formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "infoBalloonText": "Enter the approximate time you started to see the error.",
            "required": true
        },
        {
            "id": "target_server",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What is the target server?",
            "infoBalloonText": "Enter the target server name where you want to geo-restore.",
            "required": false
        },
        {
            "id": "servicetier_dropdown",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "What is the target service tier",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Select the target service tier",
			"dropdownOptions": [
                {
                    "value": "Basic",
                    "text": "Basic"
                },
                {
                    "value": "Standard",
                    "text": "Standard"
                },
                {
                    "value": "Premium",
					"text": "Premium"
                },
                {
                    "value": "vCore General Purpose",
                    "text": "vCore General Purpose"
                },
                {
                    "value": "vCore Business Critical",
                    "text": "vCore Business Critical"
                },
                {
                    "value": "Hyperscale",
                    "text": "Hyperscale"
                },
		{
                    "value": "dont_know_answer",
                    "text": "Dont know answer"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional context for the error message you are encountering.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Please provide the full error you are receiving. If available,please attach any relevant screenshots and scripts that you have used."
        }
    ]
}
---
