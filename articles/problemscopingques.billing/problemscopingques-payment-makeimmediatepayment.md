<properties
	pageTitle="Make Immediate Payment"
	description="Make Immediate Payment"
	articleId="payment-makeimmediatepaymentproblemscopingquestions"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32632937"
	productPesIds="15659"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="ASMS_Billing"
/>

# Make Immediate Payment
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Make Immediate Payment",
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
            "id": "subscriptionid_details",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "Subscription ID",
            "watermarkText": "Provide your Subscription id",
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
            "id": "invoiceid_details",
            "order": 4,
            "controlType": "textbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Invoice ID related to the issue",
            "watermarkText": "Provide your Invoice ID related to the issue",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Reason for immediate payment",
            "watermarkText": "Provide the reason for immediate payment",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
