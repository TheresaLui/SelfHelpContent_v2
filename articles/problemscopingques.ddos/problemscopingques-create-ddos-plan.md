<properties
	articleId="problemscopingques-create-ddos-plan"
	pageTitle="Scoping Questions for Create DDoS Plan"
	description="Scoping Questions for Create DDoS Plan"
	authors="karenhammons"
	ms.author="karenha,moghosal"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32680994"
	productPesIds="16355"
	cloudEnvironments="public,mooncake,fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="CloudNet_AzureDDoSProtection"
/>
# Create DDoS Plan
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Create DDoS Plan",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "public_ip",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Do you have a virtual network with public IP configured?  If yes, please enter the IP address.",
            "watermarkText": "If yes, please enter the public IP address. Example: 13.0.1.2",
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
