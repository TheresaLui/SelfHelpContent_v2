<properties
	pageTitle="Geo-replication"
	description="Scoping questions to capture more details about errors\issues encountered while geo-replicating SQL DB"
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
            "id": "SLO_dropdown",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is the secondary on the same service tier as primary",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Secondary database should always be on the same or higher SLO as primary",
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
            "watermarkText": "Please provide the full error that you seeing \ Explain your issue in detail.If available, please attach any relevant screenshots and scripts that you have used."
        }
    ],
    "$schema": "SelfHelpContent"
}
---
