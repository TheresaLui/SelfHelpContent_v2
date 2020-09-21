<properties
	pageTitle="Scoping Questions for Data Box encryption using customer manager key"
	description="Scoping Questions for Data Box encryption using customer managed key"
	authors="ansubram"
	ms.author="ansubram"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32743107"
	productPesIds="16505"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="32743107"
	ownershipId="StorageMediaEdge_DataBox"
/>
# Data Box issues with customer managed key
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Data Box issues - Encryption using customer managed key",
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
            "id": "cmk_access",
            "order": 200,
            "controlType": "dropdown",
            "displayLabel": "If there was an issue with the key in your key vault used for this order, was it recoverable?",
	          "watermarkText": "Choose an option",
            "dropdownOptions": [
            {
                "value" : "Yes",
                "text" : "Yes"
            },
            {
                "value" : "No",
                "text" : "No"
            },
            {
                "value" : "dont_know_answer",
                "text" : "Other, don't know or not applicable"
            }
          ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 600,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide any additional details regarding the issue such as issue encountered with the customer managed key and other relevant information",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "learn_more_text",
            "order": 700,
            "controlType": "infoblock",
            "content": "<a href='https://docs.microsoft.com/azure/databox/data-box-customer-managed-encryption-key-portal'>Learn more</a> about using customer managed keys for Azure Data Box"
        }
	],
	"$schema": "SelfHelpContent"
}
---
