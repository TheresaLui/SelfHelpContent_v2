<properties
	articleId="f91ecff3-6a0b-4013-9e61-fc57f2aacd5b"
	pageTitle="Scoping Questions for Configure DDoS protection standard issue"
	description="Scoping Questions for Configure DDoS protection standard Issue"
	authors="genlin"
	ms.author="mariliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32605607"
	productPesIds="16355"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="CloudNet_AzureDDoSProtection"
/>
# DDOS Protection\\Configure DDoS protection standard
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Configure DDoS protection standard",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "is_it_first_time_deployed",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Are you activating DDoS Standard for the first time?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "dont_know_answer",
                    "text": "No"
                }
            ],
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
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
