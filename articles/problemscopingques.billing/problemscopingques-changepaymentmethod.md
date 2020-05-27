<properties
	pageTitle="Change Payment Method"
	description="Change Payment Method"
	articleId="changepaymentmethod"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32632934"
	productPesIds="15659"
	cloudEnvironments="public, Mooncake, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="ASMS_Billing"
/>

# Change Payment Method
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Change Payment Method",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Problem Start Date",
            "required": true
        },
        {
            "id": "payment_method",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Choose the type of Payment Method",
            "watermarkText": "Choose the type of Payment Method",
            "dropdownOptions": [
                {
                    "value": "Invoice",
                    "text": "Invoice"
                },
                {
                    "value": "Credit Card",
                    "text": "Credit Card"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "browser_details1",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Browser Information",
            "watermarkText": "Choose the browser",
            "dropdownOptions": [
                {
                    "value": "Apple Safari",
                    "text": "Apple Safari"
                },
                {
                    "value": "Google Chrome",
                    "text": "Google Chrome"
                },
                {
                    "value": "Internet Explorer",
                    "text": "Internet Explorer"
                },
                {
                    "value": "Microsoft Edge",
                    "text": "Microsoft Edge"
                },
                {
                    "value": "Mozilla Firefox",
                    "text": "Mozilla Firefox"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "browser_details2",
            "order": 4,
            "visibility": "browser_details1 == Other",
            "controlType": "textbox",
            "displayLabel": "Please provide the Browser Information",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Error message (if applicable)",
            "watermarkText": "Provide any error message or additional information about your issue",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
