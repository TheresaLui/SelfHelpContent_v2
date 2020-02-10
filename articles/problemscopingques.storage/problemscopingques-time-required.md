<properties
	pageTitle="Storage issue with date time"
	description="Storage issue with date time scoping question"
	authors="Sijia"
    	ms.author="siz"
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
            "id": "azcopy_performance",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are you experiencing any performance issue with the copy operations",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "yes",
                    "text": "Yes"
                },
                {
                    "value": "no",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know or not listed above"
                }
            ],
            "required": true
        },
        {
            "id": "error_code",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Did you receive any error code? ",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "error400",
                    "text": "400 - Bad Request"
                },
                {
                    "value": "error401",
                    "text": "401 – Unauthorized"
                },
                {
                    "value": "error403",
                    "text": "403 – Forbidden"
                },
                {
                    "value": "error404",
                    "text": "404 - Resource not found (Authentication)"
                },
                {
                    "value": "error409",
                    "text": "409 - Conflict"
                },
                {
                    "value": "error412",
                    "text": "412 – Precondition failed"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know or not listed above"
                }
            ],
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate start time of the most recent occurrence",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType":"multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
