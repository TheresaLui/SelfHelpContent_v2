<properties
	articleId="problemscopingques-netappvolume-createdualprotocol"
	pageTitle="Issue while creating dual protocol volume"
	description="Issue while creating dual protocol volume"
	authors="b-kiudup"
	ms.author="b-kiudup"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32777923"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Issue while creating dual protocol volume
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issue while creating dual protocol volume",
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
            "id": "AADDS",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is Azure ADDS used?",
            "watermarkText": "Is Azure ADDS used?",
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
            "id": "reverselookup",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is PTR of AD machine added in DNS?",
            "watermarkText": "Is PTR of AD machine added in DNS?",
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
            "required": false
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
