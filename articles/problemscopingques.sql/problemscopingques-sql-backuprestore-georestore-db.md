<properties
	pageTitle="Error while Geo-restore"
	description="Scoping questions to capture more details about errors encountered while trying to Geo-restore SQL DB"
	authors="andikshi"
	ms.author="andikshi"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630425"
	productPesIds="13491"
	cloudEnvironments="Public"
	schemaVersion="1"
	articleId="problem-scopingques-sql-backuprestore-georestore-db"
/>
# Error When Connecting to my Database
---
{
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "infoBalloonText": "Enter the approximate time you started to see the error.",
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "target_server",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What is the target server?",
            "infoBalloonText": "Enter wthe target server name , where you want to do the geo-restore.",
            "required": false,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "error_dropdown",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "What is the target SLO",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Select the target SLO",
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
                    "value": "Vcore-GeneralPurpose",
                    "text": "VCore-GeneralPurpose"
                },
                {
                    "value": "VCore-BusinessCritical",
                    "text": "VCore-BusinessCritical"
                },
                {
                    "value": "Hyperscale",
                    "text": "Hyperscale"
                }    
            ],
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional context for the error message you are encountering.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Always provide the full error text from the underlying client library (e.g., SqlClient), not the general error from your client application.  If available, include the client stack trace as well."
        }
    ],
    "$schema": "SelfHelpContent"
}
---
