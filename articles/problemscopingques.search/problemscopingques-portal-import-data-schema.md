<properties
	pageTitle="Portal import data wizard not suggesting the index schema"
	description="Portal import data wizard not suggesting the correct index schema"
	authors="liamca"
	ms.author="liamca"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681349"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="b364a056-f57e-4cd8-8388-6aa3d2a2deff"
	ownershipId="AzureSearch_AzureSearch"
/>
# Portal import data wizard not suggesting the correct index schema
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Portal import data wizard not suggesting the index schema",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Please describe the issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "index_name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "If applicable, please add the index name where the problem occured",
            "required": false
        },
		{
            "id": "issue_choice",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Does this issue happen consistently?",
            "watermarkText": "Choose an option",
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
                    "text": "Don't Know"
                }
            ],
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem last occur?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---