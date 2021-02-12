<properties
	pageTitle="Scoping Questions for Data Box Data copy and validation"
	description="Scoping Questions for Data Box Data copy and validation"
	authors="ansubram"
	ms.author="ansubram"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32639189,32639190,32639193,32639197,32639199,32639203,32639188,32639211"
	productPesIds="16505"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="32639189886"
	ownershipId="StorageMediaEdge_DataBox"
/>
# Data Box issues with data copy and validation
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Data Box issues - Data copy and validation",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When was the problem first observed?",
            "required": true
        },
        {
            "id": "were_changes_done",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Were there any changes done, post which you started seeing this issue?",
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
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "previous_solution",
            "visibility": "were_changes_done == Yes",
            "order": 110,
            "controlType": "multilinetextbox",
            "displayLabel": "List the changes which were made",
            "watermarkText": "Describe in detail the changes which were made",
            "required": true
        },
	{
            "id": "copy_method_used",
            "order": 200,
            "controlType": "multilinetextbox",
            "displayLabel": "What was the copy method used?",
	    "watermarkText": "Example - Robocopy (Windows), rsync/FreeFileSync/Unison/Ultracopier (Linux) or others",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 600,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide any additional details regarding the issue such as type of data being copied (blobs/files etc), number of objects and typical object size, data ports being used and and any other relevant information",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "learn_more_text",
            "order": 700,
            "controlType": "infoblock",
            "content": "<a href='https://docs.microsoft.com/azure/databox/data-box-faq'>Learn more</a> about Azure Data Box"
        }
	],
	"$schema": "SelfHelpContent"
}
---
