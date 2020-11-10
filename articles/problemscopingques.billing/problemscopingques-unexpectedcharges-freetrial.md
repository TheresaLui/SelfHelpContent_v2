<properties
	pageTitle="Unexpected Charges-free trial"
	description="Unexpected Charges-free trial"
	articleId="unexpectedcharges-problemscopingquestions-free trial"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32680681,32680680"
	productPesIds="15659"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="ASMS_Billing"
/>
# Unexpected Charges-free trial
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Unexpected Charges-free trial",
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
            "order": 8,
            "controlType": "textbox",
            "displayLabel": "Subscription ID",
            "watermarkText": "Provide your Subscription id",
            "required": true
        },
        {
            "id": "invoiceid_details",
            "order": 5,
            "controlType": "textbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Invoice ID related to the issue",
            "watermarkText": "Provide the Invoice ID related to the issue",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Describe your problem, providing as much detail as possible",
            "watermarkText": "",
            "hints": [
                {
                    "text": "Learn more: <a href='https://docs.microsoft.com/azure/billing/billing-avoid-charges-free-account'> Avoid charges with Azure free account </a>."
                },
		 {
                    "text": "Learn more: <a href='https://docs.microsoft.com/azure/billing/billing-understand-your-usage'> Understand your charge</a>."
                }
            ],
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
