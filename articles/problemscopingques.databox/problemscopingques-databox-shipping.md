<properties
	articleId="3263920091"
	pageTitle="Scoping Questions for problems with the shipment"
	description="Scoping Questions for problems with the shipment"
	authors="shijojoy"
	ms.author="shijoy"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32639209"
	productPesIds="16505"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="StorageMediaEdge_DataBox"
/>
# Missing parts once the shipment has arrived
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Shipment is damaged or tampered",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the shipment reach?",
            "required": true
        },
        {
            "id": "issue",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What is the problem with the shipment?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Damaged",
                    "text": "Damaged"
                },
                {
                    "value": "Tampered",
                    "text": "Tampered"
                },
                {
                    "value": "Missing accessories",
                    "text": "Missing accessories"
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
            "visibility": "issue == Missing accessories",
            "order": 110,
            "controlType": "multilinetextbox",
            "displayLabel": "What accessories are missing from the shipment?",
            "watermarkText": "List out the accessories missing from the shipment",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 600,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide the state in which the shipment arrived and also upload any supporting proofs",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "learn_more_text",
            "order": 700,
            "controlType": "infoblock",
            "content": "<a href='https://docs.microsoft.com/azure/databox/data-box-faq'>Learn more</a>"
        }
    ],
    "$schema": "SelfHelpContent"
}
---
