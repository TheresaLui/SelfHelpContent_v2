<properties
	articleId="f11ecff3-4011-1111-9e61-fc57f2aacd5b"
	pageTitle="Scoping Questions for under Attack with General Questions or No resource available"
	description="Scoping Questions for under Attack with General Questions or No resource available"
	authors="genlin"
	ms.author="mariliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32640594"
	productPesIds="16355"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="CloudNet_AzureDDoSProtection"
/>
# Under Attack with General Questions or No resource available
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Under Attack with General Questions or No resource available",
    "fileAttachmentHint": "",
    "formElements": [
          {
            "id": "has_vnetwithpublicip",
            "order": 1,
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
            "id": "is_publicip_attack",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is the public IP that you are trying to configure under attack?",
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
            "visibility": "is_publicip_attack == Yes",
            "controlType": "textbox",
            "displayLabel": "What public IP address is under attack?",
            "watermarkText": "Enter the public IP address. Example: 13.0.1.2",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue, or general question about the product.",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
