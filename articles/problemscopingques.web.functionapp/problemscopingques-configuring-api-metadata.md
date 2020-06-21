<properties
	articleId="problemscopingques-configuring-api-metadata"
	pageTitle="Configuring API metadata"
	description="Configuring API metadata"
	supportTopicIds="32518046"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="16072"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_AppService"
/>
# Configuring API metadata
---
{
    "resourceRequired": false,
    "title": "Configuring API metadata",
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
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the function.json file",
            "watermarkText": "function.json...",
            "required": false
        },
        {
            "id": "3",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the proxies.json file",
            "watermarkText": "proxies.json...",
            "required": false
        },
        {
            "id": "4",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the auto generated YAML file",
            "watermarkText": "yaml file...",
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
