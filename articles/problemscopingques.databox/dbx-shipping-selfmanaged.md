<properties
	articleId="32743105_psq"
	pageTitle="Scoping Questions for self managed shipping issues"
	description="Scoping Questions for self managed shipping issues"
	authors="ansubram"
	ms.author="ansubram"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32743105"
	productPesIds="16505"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
  ownershipId="StorageMediaEdge_DataBox"
/>
# Data Box and Data Box Disk self managed shipping
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Data Box/Disk issues with self-managed shipping",
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
            "id": "shipping_stage",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Select shipping stage",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Pick-up from Azure datacenter",
                    "text": "Pick-up from Azure datacenter"
                },
                {
                    "value": "Drop-off to Azure datacenter",
                    "text": "Drop-off to Azure datacenter"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "is_pickupauthcode_visible",
            "visibility": "shipping_stage == Pick-up from Azure datacenter",
            "order": 110,
            "controlType": "dropdown",
            "displayLabel": "Is the Authorization code visible in the Azure portal under Schedule pickup?",
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
            "id": "is_dropoffauthcode_visible",
            "visibility": "shipping_stage == Drop-off to Azure datacenter",
            "order": 210,
            "controlType": "dropdown",
            "displayLabel": "If this is a Data Box Import to Azure order, did Prepare to Ship complete successfully?",
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
            "watermarkText": "Please provide any additional details regarding the issue with self-managed shipping",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
