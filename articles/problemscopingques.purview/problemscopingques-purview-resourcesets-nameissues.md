<properties
	articleId="ae64770f-4755-4c82-ae26-dd4749e569f2"
	pageTitle="Scoping Questions for Purview resource sets - names issues"
	description="Scoping Questions for Purview resource sets - names issues"
	authors="deeptivu"
	ms.author="deeptivu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32783240,32783241"
	productPesIds="17354"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_ProjectBabylon"
/>
# Scoping Questions for Purview resource sets - names issues
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Azure Purview Cannot Create Account",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate time when the problem stopped occurring. If the issue is ongoing, leave this field blank",
            "required": false
        },
         {
            "id": "problem_description",
            "order": 10,
            "controlType": "multilinetextbox",
            "displayLabel": "Brief description of the issue",
            "watermarkText": "Please provide any information related to this issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "catalog_name",
            "order": 20,
            "controlType": "textbox",
            "displayLabel": "Name of the catalog",
            "required": false
        },
        {
            "id": "new_values",
            "order": 30,
            "controlType": "textbox",
            "displayLabel": "The new values that are put in for the scoped resource set policy",
            "required": false
        },
        {
            "id": "asset_uri",
            "order": 40,
            "controlType": "textbox",
            "displayLabel": "Sample Asset URIs",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
