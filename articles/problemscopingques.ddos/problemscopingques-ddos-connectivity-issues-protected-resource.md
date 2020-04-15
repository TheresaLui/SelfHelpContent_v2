<properties
	articleId="f11ecff3-3003-1111-9e61-fc57f2aacd5b"
	pageTitle="Scoping Questions for configuring protection on Virtual Network resource"
	description="Scoping Questions for configuring protection on Virtual Network resource"
	authors="genlin"
	ms.author="mariliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32605609"
	productPesIds="16355"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="CloudNet_AzureDDoSProtection"
/>
# Configure protection on Virtual Network resource
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Configure protection on Virtual Network resource",
    "fileAttachmentHint": "",
    "formElements": [
          {
            "id": "has_publicIP",
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
            "id": "what_publicip",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What is the public IP that has connectivity issue?",
            "watermarkText": "Enter the public IP address. Example: 13.0.1.2",
            "required": false
        },
        {
            "id": "what_vnet",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the virtual network resource that has connectivity issue?",
            "watermarkText": "Enter the name of the virtual network resource",
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
