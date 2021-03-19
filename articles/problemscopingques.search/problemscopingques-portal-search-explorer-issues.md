<properties
	pageTitle="Portal/Search Explorer issues"
	description="Issues with Azure Cognitive Search portal search explorer"
	authors="liamca"
	ms.author="liamca"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681383"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="0e9a278b-ccb9-4176-8272-d8d6390d8d19"
	ownershipId="AzureSearch_AzureSearch"
/>
# Portal/Search Explorer search query issue
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issues with Azure Cognitive Search portal search explorer",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Please describe the issue you had using the Cognitive Search Portal Explorer",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "index_name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Please add the index name where the problem occured",
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