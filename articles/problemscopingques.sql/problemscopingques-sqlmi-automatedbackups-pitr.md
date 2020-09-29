<properties
	pageTitle="Automated backups or point-in-time restore"
	description="Scoping questions to capture more details about errors encountered while trying to do a PITR"
	authors="andikshi,vitomaz-msft,MladjoA"
	ms.author="vitomaz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32637234"
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-sqlmi-automatedbackups-pitr"
	ownershipId="AzureData_AzureSQLMI"
/>
# Error with automated backups or point-in-time restore
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
            "infoBalloonText": "Enter the approximate time you started to see the error",
            "required": true
        },
        {
            "id": "issue_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is the issue with automated backups or point-in-time restore?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Choose the issue type",
            "dropdownOptions": [
                {
                    "value": "Automated Backups",
                    "text": "Automated Backups"
                },
                {
                    "value": "Point-in-time restore",
                    "text": "Point-in-time restore"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "restore_time",
            "order": 3,
            "controlType": "datetimepicker",
            "visibility": "issue_type==Point-in-time restore",
            "displayLabel": "What was the requested restore datetime?",
            "infoBalloonText": "Enter the approximate time that you want the point-in-time restore for",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional context for the error message you are encountering",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Please provide the full error you are receiving. If available, please attach any relevant screenshots and scripts that you have used."
        }
    ]
}
---
