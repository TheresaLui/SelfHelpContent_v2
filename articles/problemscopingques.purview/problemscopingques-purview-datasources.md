<properties
	articleId="70dd1924-d236-465b-96b5-bd440419565a"
	pageTitle="Scoping Questions for Purview Data Sources"
	description="Scoping Questions for Purview Data Sources"
	authors="deeptivu"
	ms.author="deeptivu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32783198,32783225,32783258"
	productPesIds="17354"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_ProjectBabylon"
/>
# Purview Data Sources
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Azure Purview Data Sources",
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
            "id": "error_message",
            "order": 40,
            "controlType": "textbox",
            "displayLabel": "Complete error message (if any)",
            "required": false
        },
        {
            "id": "type_region",
            "order": 50,
            "controlType": "textbox",
            "displayLabel": "What is the type and Region or location of the Data Source?",
            "required": true
        },
       {
            "id": "frequency",
            "order": 60,
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
        },
        {
            "id": "other_services",
            "order": 70,
            "controlType": "textbox",
            "displayLabel": "Are you able to connect to the Data Source from other Azure services like Data Factory or Data Share?",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
