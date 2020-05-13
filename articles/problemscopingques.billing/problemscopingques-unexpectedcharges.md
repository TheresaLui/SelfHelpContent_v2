<properties
	pageTitle="Unexpected Charges"
	description="Unexpected Charges"
	articleId="unexpectedcharges-problemscopingquestions"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32632931"
	productPesIds="15659"
	cloudEnvironments="public, Mooncake, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="ASMS_Billing"
/>
# Unexpected Charges
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Unexpected Charges",
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
            "id": "service_details",
            "order": 3,
            "controlType": "textbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Service causing the charges",
            "watermarkText": "Provide the Service causing the charges",
            "required": false
        },
        {
            "id": "impact_details",
            "order": 4,
            "controlType": "textbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Impacted duration",
            "watermarkText": "Provide the Impacted duration",
            "required": false
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
            "displayLabel": "Brief summary of the issue",
            "watermarkText": "Provide brief summary of the issue",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
