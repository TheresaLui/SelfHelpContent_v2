<properties
	articleId="problemscopingques-delete-ddos-plan"
	pageTitle="Scoping Questions for Delete DDoS Plan"
	description="Scoping Questions for Delete DDoS Plan"
	authors="karenhammons"
	ms.author="karenha,moghosal"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32680995"
	productPesIds="16355"
	cloudEnvironments="public,mooncake,fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="CloudNet_AzureDDoSProtection"
/>
# Delete DDoS Plan
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Create DDoS Plan",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "disassociate_vnet",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Did you disassociate all virtual networks with DDoS protection enabled?",
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
