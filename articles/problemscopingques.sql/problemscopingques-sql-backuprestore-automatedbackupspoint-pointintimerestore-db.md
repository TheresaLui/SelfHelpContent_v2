<properties
	pageTitle="Automated backups or point in time restore"
	description="Scoping questions to capture more details about errors encountered while trying to do a PITR for SQL DB"
	authors="andikshi"
	ms.author="andikshi"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32688667"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="problem-scopingques-sql-automatedbackupspoint-pointintimerestore-db"
	ownershipId="AzureData_AzureSQLDB"
/>
# Error with automatedbackupspoint- pointintimerestore-db
---
{
	"$schema": "SelfHelpContent",
	"resourceRequired": false,
	"subscriptionRequired": false,
	"formElements": [{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "What is the start time of the issue?",
			"required": true
		}, {
			"id": "problem_end_time",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "What is the end time of the issue? (If ongoing, leave this field blank)",
			"required": false
					},
	{
            "id": "IssueType_dropdown",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is the issue with Backups or Point in time restore",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Choose the issue type",
			"dropdownOptions": [
                {
                    "value": "Backups",
                    "text": "Backups"
                },
                {
                    "value": "Point in time restore",
                    "text": "Point in time restore"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Dont know answer"
                }
            ],
            "required": true
        },
	{
            "id": "restore_time",
            "order": 4,
            "controlType": "datetimepicker",
	    "visibility": "IssueType_dropdown==Point in time restore",
            "displayLabel": "What was the requested restore datetime?",
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
            "watermarkText": "Please provide the full error you are receiving. If available,please attach any relevant screenshots and scripts that you have used."
        }
    ]
}
---
