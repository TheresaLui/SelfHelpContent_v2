<properties
	pageTitle="Unexpected Charges - cancelled service"
	description="Unexpected Charges- cancelled service"
	articleId="unexpectedcharges-problemscopingquestions-cancelled-service"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32680682"
	productPesIds="15659"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="ASMS_Billing"
/>
# Unexpected Charges-cancelled service
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Unexpected Charges-cancelled service",
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
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Subscription ID",
            "watermarkText": "Provide your Subscription id",
            "required": false
        },
        {
            "id": "service_details",
            "order": 3,
            "controlType": "textbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Name of the service",
            "watermarkText": "",
            "required": true
        },
        {
            "id": "problem_description1",
            "order": 4,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": false,
            "displayLabel": "Screenshot of the portal that service is cancelled",
            "watermarkText": "",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
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
