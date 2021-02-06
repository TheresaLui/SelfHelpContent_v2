<properties
	articleId="9ae9201c-c966-43ee-9ea0-050ac6f85a03"
	pageTitle="Scoping Questions for Purview - I set my scoped resource set policy "
	description="Scoping Questions for Purview - I set my scoped resource set policy"
	authors="deeptivu"
	ms.author="deeptivu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32783240,32783241"
	productPesIds="17354"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_ProjectBabylon"
/>
# Purview - I set my scoped resource set policy 
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Azure Purview - I set my scoped resource set policy",
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
            "order": 40,
            "controlType": "textbox",
            "displayLabel": "Name of the catalog",
            "required": false
        },
        {
            "id": "new-values",
            "order": 50,
            "controlType": "textbox",
            "displayLabel": "The new values put in for the scoped resource set policy",
            "required": false
        },
         {
            "id": "sample",
            "order": 60,
            "controlType": "textbox",
            "displayLabel": "Sample Asset URIs",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
