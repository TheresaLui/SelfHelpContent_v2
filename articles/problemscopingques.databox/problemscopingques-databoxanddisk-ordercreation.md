<properties
	articleId="326392008"
	pageTitle="Scoping Questions for order creation issues"
	description="Scoping Questions for order creation issues"
	authors="madhurinms"
	ms.author="madhn"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32639192"
	productPesIds="16505"
	cloudEnvironments="public, Fairfax"
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
                    "value": "Unable to proceed further due to Portal validation",
                    "text": "Unable to proceed further due to Portal validation"
                },
                {
                    "value": "Deployment failed at the end of create flow",
                    "text": "Deployment failed at the end of create flow"
                },
                {
                    "value": "Ordering not available for my country and target Azure region",
                    "text": "Ordering not available for my country and target Azure region"
                },
                {
                    "value": "Ordering not available for my subsription type",
                    "text": "Ordering not available for my subscription type"
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
