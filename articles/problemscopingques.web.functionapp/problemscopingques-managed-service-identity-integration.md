<properties
	articleId="problemscopingques-managed-service-identity-integration"
	pageTitle="Managed Service Identity (MSI) Integration"
	description="Managed Service Identity (MSI) Integration"
	supportTopicIds="32608573"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="16072"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_AppService"
/>
# Managed Service Identity (MSI) Integration
---
{
    "resourceRequired": false,
    "title": "Managed Service Identity (MSI) Integration",
    "fileAttachmentHint": "Please attach any relevant logs/screenshots",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Incident time",
            "required": true
        },
        {
            "id": "2",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are you attempting to authenticate inbound requests to your Function App or authorize the Function on other Azure resources?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Authenticate inbound requests",
                    "text": "Authenticate inbound requests"
                },
                {
                    "value": "Authorize the Function on other Azure resources",
                    "text": "Authorize the Function on other Azure resources"
                }
            ],
            "required": false
        },
        {
            "id": "3",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What exception are you experiencing?",
            "watermarkText": "exception...",
            "required": false
        },
        {
            "id": "4",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Which Azure feature are you attempting to interface with via the MSI configuration? ",
            "watermarkText": "...",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your issue including any error messages you are seeing.",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
