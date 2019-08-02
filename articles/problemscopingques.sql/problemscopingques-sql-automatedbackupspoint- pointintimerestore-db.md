<properties
	pageTitle="Error with automatedbackupspoint- pointintimerestore-db"
	description="Scoping questions to capture more details about errors encountered while trying to Geo-restore SQL DB"
	authors="andikshi"
	ms.author="andikshi"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630409"
	productPesIds="13491"
	cloudEnvironments="Public"
	schemaVersion="1"
	articleId="problem-scopingques-sql-automatedbackupspoint-pointintimerestore-db"
/>
# Error with automatedbackupspoint- pointintimerestore-db
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
            "id": "restore_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "What was the requested restore date\time?",
            "infoBalloonText": "Enter the approximate time that you want the point in time restore for",
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
