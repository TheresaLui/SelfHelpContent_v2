<properties
	articleId="f12ecff3-6a0b-1111-9e61-fc57f2aacd5b"
	pageTitle="Scoping Questions for configure DDoS Alert issue"
	description="Scoping Questions for configure DDoS Alert issue"
	authors="TobyTu"
	ms.author="mariliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32640597"
	productPesIds="16355"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Configure DDoS Alert
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Configure DDoS Alert",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "public_ip",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "What is the public IP you want to configure?",
            "watermarkText": "Enter the public IP address. Example: 13.0.1.2",
            "required": false
        },
        {
            "id": "under_attack",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is the public IP you are trying to configure under attack?",
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
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 4,
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
