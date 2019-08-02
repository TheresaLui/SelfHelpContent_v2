<properties
	pageTitle="Error while Geo-replication"
	description="Scoping questions to capture more details about errors encountered while trying to Geo-restore SQL DB"
	authors="andikshi"
	ms.author="andikshi"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630424"
	productPesIds="13491"
	cloudEnvironments="Public"
	schemaVersion="1"
	articleId="problem-scopingques-sql-backuprestore-georeplication-db"
/>
# Error when trying to geo-replication
---
{
	"resourceRequired": true,
	"subscriptionRequired": true,
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
            "id": "error_dropdown",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is the secondry on the same service tier as primary",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Secondry database should always be on the same of higher SLO as primary",
			"dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
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
            "watermarkText": "Always provide the full error text from the underlying client library (e.g., SqlClient), not the general error from your client application.  If available, include the client stack trace as well."
        }
    ],
    "$schema": "SelfHelpContent"
}
---
