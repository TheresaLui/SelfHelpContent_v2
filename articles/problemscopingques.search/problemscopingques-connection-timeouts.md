<properties
	pageTitle="Connection timeouts"
	description="Connection timeouts"
	authors="mcarter"
	ms.author="mcarter"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681345"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="fbbc6b2a-ff8b-464a-806e-e29126426877"
	ownershipId="AzureSearch_AzureSearch"
/>
# Connection timeouts
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Connection timeouts",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe the timeout issue you experienced",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText":"Please provide the full error text when possible."
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "infoBalloonText": "Enter the approximate time you started to see the error.",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem stop? (If ongoing, leave this field blank)",
            "infoBalloonText": "Enter when the error stopped.  (Leave blank if the issue is ongoing)",
            "required": false
        },
        {
            "id": "is_reproducible",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Is the problem reproducable?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "yes",
                    "text": "Yes, we can reproduce the problem consistently"
                },
                {
                    "value": "no",
                    "text": " No. The problem occurs randomly"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
            ],
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
