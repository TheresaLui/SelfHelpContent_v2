<properties
	pageTitle="Scoping questions for Pay by InvoiceStorage/Development"
	description="Scoping questions for Pay by Invoice"
	authors="prdasneo"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32454866"
	productPesIds="15659"
	cloudEnvironments="public"
   schemaVersion="1"
   articleId="10ced282-0269-4229-86c4-5cdb943f83dd"
	ownershipId="ASMS_Billing"
/>

# Pay by Invoice

---
{
    "resourceRequired": false,
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": [
                {
                    "text": "Enter the following information"
                },
                {
                    "text": "Company name"
                },
                {
                    "text": "Billing address"
                },
                {
                    "text": "<a href='https://docs.microsoft.com/azure/billing/billing-add-change-azure-subscription-administrator#check-the-account-administrator-of-the-subscription'>Account administrator's email address</a>"
                }
            ]
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---