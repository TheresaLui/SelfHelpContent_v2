<properties
	articleId="326392007"
	pageTitle="Scoping Questions for order delivery"
	description="Scoping Questions for order delivery"
	authors="madhurinms"
	ms.author="madhn"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32639213"
	productPesIds="16505"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
    ownershipId="StorageMediaEdge_DataBox"
/>
# Data Box Disk slow copy speed
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Data Box/Disk oder delivery",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate time when the problem stopped occurring. If the issue is ongoing, leave this field blank",
            "required": false
        },
        {
            "id": "is_order_status_shipped",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Provide more details",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Order has shipped from Azure 5 days ago but I have not received it",
                    "text": "Order has shipped from Azure 5 days ago but I have not received it"
                },
                {
                    "value": "I ordered more than 7 days ago but it has not been shipped",
                    "text": "I ordered more than 7 days ago but it has not been shipped"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "is_carrier_contacted",
            "visibility": "is_order_status_shipped == Order has shipped from Azure 5 days ago but I have not received it",
            "order": 110,
            "controlType": "dropdown",
            "displayLabel": "Did you contact the carrier?",
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
            "id": "problem_description",
            "order": 600,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide full error text and any other relevant information",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
