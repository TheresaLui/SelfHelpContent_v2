<properties
	articleId="problemscopingques-netappvolume-backupnotworking"
	pageTitle="Backup not working after policy assignment"
	description="Backup not working after policy assignment"
	authors="b-avaish"
	ms.author="b-avaish"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32784804"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Backup not working after policy assignment
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Backup not working after policy assignment",
    "fileAttachmentHint": "",
    "formElements": [
		{
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
		{
            "id": "policy_state",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are the policy state of assigned backup policy and snapshot policy enabled?",
            "watermarkText": "Are the policy state of assigned backup policy and snapshot policy enabled?",
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
                    "text": "None of the above"
                }
			],
            "required": true
        },
		{
        "id": "configure_backups",
        "order": 3,
        "controlType": "dropdown",
        "displayLabel": "What is the policy state in configure backups of a volume",
        "watermarkText": "Choose an option",
        "dropdownOptions": [{
            "value": "Suspend",
            "text": "Suspend"
        }, {
            "value": "Resume",
            "text": "Resume"
        }, {
            "value": "dont_know_answer",
            "text": "None of the above"
        }],
        "required": true
	},
	{
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---