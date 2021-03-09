<properties
	articleId="7b985a79-2b6a-4ca3-b4bd-a93c45c76926"
	pageTitle="Scoping Questions for Purview Scan RUle Sets Authentication Fialed"
	description="Scoping Questions for Purview Scan RUle Sets Authentication Fialed"
	authors="deeptivu"
	ms.author="deeptivu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32783206"
	productPesIds="17354"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_ProjectBabylon"
/>
# Scoping Questions for Purview Scan RUle Sets Authentication Fialed
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
            "id": "error",
            "order": 20,
            "controlType": "textbox",
            "displayLabel": "Complete error message (if any)",
            "required": false
        },
        {
            "id": "scan_id",
            "order": 30,
            "controlType": "textbox",
            "displayLabel": "Provide Scan Run ID",
            "required": false
        },
       {
            "id": "data_source",
            "order": 40,
            "controlType": "textbox",
            "displayLabel": "What is the type of the Data Source?",
            "required": true
        },
        {
            "id": "frequency",
            "order": 50,
            "controlType": "dropdown",
            "displayLabel": "Is this issue intermittent or consistent?",
            "watermarkText": "Choose an option",
             "dropdownOptions": [
                {
                    "value": "Intermittent",
                    "text": "Intermittent"
                },
                {
                    "value": "Consistent",
                    "text": "Consistent"
                },
		{
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
