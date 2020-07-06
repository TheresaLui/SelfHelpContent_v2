<properties
	pageTitle="Scoping Questions for Data Box Data copy and validation - Issue with exported data"
	description="Scoping Questions for Data Box Data copy and validation - Issue with exported data"
	authors="ansubram"
	ms.author="ansubram"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32743104"
	productPesIds="16505"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="32743104"
	ownershipId="StorageMediaEdge_DataBox"
/>
# Data Box issues with data copy and validation in Data export
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Data Box issues - Data copy and validation - Issue with exported data",
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
            "id": "exported_data",
            "order": 200,
            "controlType": "dropdown",
            "displayLabel": "Select the issue category with the exported data",
            "watermarkText": "Choose an option",
             "dropdownOptions": [
                {
                    "value": "Data not exported",
                    "text": "Some data selected while ordering did not get exported to the device"
                },
                {
                    "value": "Log files",
                    "text": "Problem with the verbose or error log files"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
             ]
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
