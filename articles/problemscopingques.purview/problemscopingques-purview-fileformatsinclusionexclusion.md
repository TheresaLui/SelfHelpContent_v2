<properties
	articleId="4288abb2-bf47-44fc-92c4-a363c87fdbff"
	pageTitle="Scoping Questions for Purview File formts inclusion/exclusion"
	description="Scoping Questions for Purview File formts inclusion/exclusion"
	authors="deeptivu"
	ms.author="deeptivu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32783229,32783230"
	productPesIds="17354"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_ProjectBabylon"
/>
# Purview File formts inclusion/exclusion
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Azure Purview File formts inclusion/exclusion",
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
            "id": "file_formats",
            "order": 40,
            "controlType": "textbox",
            "displayLabel": "Which file format(s) are you trying to deselect?",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
