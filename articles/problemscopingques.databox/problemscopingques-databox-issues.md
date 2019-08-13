<properties
	pageTitle="Scoping Questions for Data Box"
	description="Scoping Questions for Data Box"
	authors="shijojoy"
	ms.author="shijoy"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32639189,32639190,32639193,32639197,32639199,32639203,32639188,32639211,32639191,32639195,32639207,32639212"
	productPesIds="16505"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="3263918912"
/>
# Data Box issues
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Data Box issues",
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
            "id": "problem_description",
            "order": 600,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide the details regarding the issue and and any other relevant information",
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
