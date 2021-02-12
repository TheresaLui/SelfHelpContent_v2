<properties
	pageTitle="Application Backup and Restore"
	description="Application Backup and Restore"
	authors="peterpogorski"
	ms.author="pepogors"
	selfHelpType="ProblemScopingQuestions"
	supportTopicIds="32608941"
	productPesIds="15842"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-backup-restore-sf"
	ownershipId="Compute_ServiceFabric"
/>
# Application Backup and Restore
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Application Backup and Restore",
    "formElements": [{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "Incident time",
			"required": true
		},
		{
			"id": "problem_description",
			"order": 2,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue including any error messages you are seeing.",
			"required": true,
			"useAsAdditionalDetails": true
		},
        {
            "id": "application_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Application Name",
            "watermarkText": "Provide the name of the application.",
            "required": false
        },
        {
            "id": "using_backup_restore",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Are you using the Backup and Restore API or the periodic Backup and Restore service?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [{
                "value": "Yes",
                "text": "Yes"
            },
            {
                "value": "No",
                "text": "No"
            }],
            "required": false
        }
	],
    "$schema": "SelfHelpContent"
}
---