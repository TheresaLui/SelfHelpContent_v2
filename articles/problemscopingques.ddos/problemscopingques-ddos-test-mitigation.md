<properties
	articleId="f11ecff3-4001-1111-9e61-fc57f2aacd5b"
	pageTitle="Scoping Questions for Test DDoS mitigation"
	description="Scoping Questions for Test DDoS mitigation"
	authors="genlin"
	ms.author="mariliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32605610"
	productPesIds="16355"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="CloudNet_AzureDDoSProtection"
/>
# Test DDoS mitigation
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Test DDoS mitigation",
    "fileAttachmentHint": "",
    "formElements": [
          {
            "id": "has_ddosplan",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Do you have a DDoS protection plan?",
            "watermarkText": "Choose an option:",
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
            "id": "has_vnetwithpublicip",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Do you have a virtual network with public IP configured?",
            "watermarkText": "Choose an option:",
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
            "id": "what_publicip_fortest",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the Public IP that you are using to test DDoS Protection?",
            "watermarkText": "Enter the public IP address. Example: 13.0.1.2",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
