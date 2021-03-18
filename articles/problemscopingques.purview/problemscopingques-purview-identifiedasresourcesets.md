<properties
	articleId="12393fe6-de28-48f2-99c6-1b5c987242e4"
	pageTitle="Scoping Questions for Purview files that incorrectly got bunched together into a resource set"
	description="Scoping Questions for Purview files that incorrectly got bunched together into a resource set"
	authors="deeptivu"
	ms.author="deeptivu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32783238,32783239"
	productPesIds="17354"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_ProjectBabylon"
/>
# Purview files that incorrectly got bunched together into a resource set
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Azure Purview files that incorrectly got bunched together into a resource set",
    "fileAttachmentHint": "In case it’s a custom classification, please add screenshot of the configured classification",
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
            "id": "url",
            "order": 40,
            "controlType": "textbox",
            "displayLabel": "The specific URL of the resource (s) that weren’t properly identified as resource sets",
            "required": false
        },
         {
            "id": "scan_id",
            "order": 50,
            "controlType": "textbox",
            "displayLabel": "If this was ingested via scan, the scan ID it was ingested with",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
