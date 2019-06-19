<properties
	pageTitle="Billing API"
	description="Billing API"
	articleId="billingapi"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32599495"
	productPesIds="15659"
	cloudEnvironments="public"
	schemaVersion="1"
/>

# Billing API
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Billing API",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "visibility": null,
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        },
        {
            "id": "SubscriptionId",
            "order": 6,
            "displayLabel": "Enter the Subscription ID",
	    "controlType": "textbox",
            "useAsAdditionalDetails": true,       
            "watermarkText": "Provide the email id accessing the data",
            "required": false
          },
        {
            "id": "subscriptionid_details",
            "order": 7,
            "visibility": "SubscriptionId == dont_know_answer",
            "controlType": "textbox",
            "displayLabel": "Subscription ID",
            "watermarkText": "Provide your Subscription id",
            "required": false
        },
        {
            "id": "emailid_details",
            "order": 3,
            "controlType": "textbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Email ID accessing the data",
            "watermarkText": "Provide the email id accessing the data",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Error Message"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
