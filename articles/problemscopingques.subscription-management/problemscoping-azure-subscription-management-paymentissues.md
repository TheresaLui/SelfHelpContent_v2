<properties
	pageTitle="Scoping questions for Issue with Azure payment issues"
	description="Scoping questions for Subscription Management/Issue with Azure payment"
	authors="prdasneo"
	ms.author="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32680691"
	productPesIds="15660"
	cloudEnvironments="public, MoonCake, Blackforest, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingquestion-paymentissues"
	ownershipId="ASMS_SubscriptionManagement"
/>

# Issue with Azure payment
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Payment Issues - Azure Subscriptions",
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
            "id": "subscription_details",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Subscription ID",
            "watermarkText": "",
            "required": true
        },
        {
            "id": "payment_method",
            "order": 3,
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
            "id": "error_details",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Error Message (if any)",
            "watermarkText": "",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Issue description",
            "watermarkText": "Provide any additional information about your issue",
            "required": true
	    }
    ],
    "$schema": "SelfHelpContent"
}
---
