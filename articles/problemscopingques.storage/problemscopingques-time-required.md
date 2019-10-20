<properties
	pageTitle="Storage issue with date time"
	description="Storage issue with date time scoping question"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602737"
	productPesIds="16459"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest"
	schemaVersion="1"
	articleId="bb8a93ca-13a4-4972-8714-eaafe179a6a9"
/>
# Storage issue with date time, migrate from external 
---
{
    "subscriptionRequired": true,"resourceRequired": true,
    "title": "Datetime required scoping question",
    "fileAttachmentHint": "",
    "formElements": [
    	{
            "id": "azcopy_command_needhelp",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Do you have questions on AzCopy command",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "yes",
                    "text": "yes"
                },
                {
                    "value": "no",
                    "text": "no"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
            ],
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate start time of the most recent occurrence",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType":"multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
