<properties
	pageTitle="Issue getting a custom skill to work"
	description="Issue getting a custom skill to work"
	authors="dereklegenzoff"
	ms.author="delegenz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681374"
	productPesIds="15568"
	cloudEnvironments="Public, FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="1404c102-0c36-4489-8e9e-0bb8692ae45e"
	ownershipId="AzureSearch_AzureSearch"
/>

# Issue getting a custom skill to work
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Issue getting a custom skill to work",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "indexer_name",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "What is the name of your indexer?",
            "required": true,
            "useAsAdditionalDetails": false
        },
        {
            "id": "skillset_name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What is the name of your skillset?",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details. Please include any error messages you see related to your custom skill.",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did you last try to run the indexer?",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---