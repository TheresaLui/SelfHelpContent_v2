<properties
	articleId="f13ecff3-6a0b-1111-9e61-fc57f2aacd5b"
	pageTitle="Scoping Questions for configure DDoS mitigation flow logs issue"
	description="Scoping Questions for configure DDoS mitigation flow logs issue"
	authors="TobyTu"
	ms.author="mariliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32640598"
	productPesIds="16355"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Configure DDoS mitigation flow logs
---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "Creating an Azure Firewall Policy",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "azure_firewall",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Is this about Azure Firewall Management using Azure Firewall Manager?",
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
            "id": "virtual_hub",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is Azure Firewall deployed in a Secured Virtual Hub?",
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
            "id": "partner_integration",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is this about a Trusted Security Partner integration with Azure Firewall Manager?",
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
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
