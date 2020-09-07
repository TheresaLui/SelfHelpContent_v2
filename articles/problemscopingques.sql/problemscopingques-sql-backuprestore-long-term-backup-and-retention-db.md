<properties
	pageTitle="Long-term backup retention"
	description="Scoping questions to capture more details about errors encountered while long-term-backup-and-retention"
	authors="andikshi"
	ms.author="andikshi"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630432"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="problem-scopingques-sql-backuprestore-long-term-backup-and-retention-db"
	ownershipId="AzureData_AzureSQLDB_BackupRestore"
/>
# Error while long-term-backup-and-retention
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
            "id": "error_dropdown",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "What is the type of issue",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Select the best most relevant issue type",
			"dropdownOptions": [
                {
                    "value": "Configuring LTR",
                    "text": "Configuring LTR"
                },
                {
                    "value": "Restoring DB from LTR",
                    "text": "Restoring DB from LTR"
                },
                {
                    "value": "Deleting LTR",
                    "text": "Deleting LTR"
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
            "watermarkText": "Please provide the full error that you are seeing or explain your issue in detail.If available, please attach any relevant screenshots and scripts that you have used."
        }
    ]
}
---
