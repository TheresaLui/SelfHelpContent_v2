<properties
	articleId="problemscopingques-misroutehandling"
	pageTitle="Azure Firewall Generic"
	description="Azure Firewall Generic"
	authors="spacest"
	ms.author="mariliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32628805,32608919,32608920,32628807,32628806,32608924,32608918,32608921,32608922,32608917"
	productPesIds="16556"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="CloudNet_AzureFirewall"
/>
# Azure Firewall Generic
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Azure Firewall Generic",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "is_it_AzureFirewall",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Is this case related to the Azure Firewall service?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "See what is <a href='https://docs.microsoft.com/azure/firewall/overview'>Azure Firewall service</a>.",
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
            "id": "is_it_deployed",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is Azure Firewall deployed in your subscription?",
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
