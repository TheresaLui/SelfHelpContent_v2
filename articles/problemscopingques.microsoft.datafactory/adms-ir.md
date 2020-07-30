<properties
	pageTitle="Azure Data Movement IR issue info"
	description="Scoping questions to gather Azure Data Movement IR issue information"
	authors="chez-charlie"
	ms.author="chez"
	selfHelpType="problemScopingQuestions"
    supportTopicIds="32629537, 32637155"
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
    articleId="c39fcac9-2658-490f-9888-e78d2b526dee"
	ownershipId="AzureData_DataFactory"
/>

# Azure Data Movement Integration Runtime Issue

---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure Data Movement IR issue",
    "fileAttachmentHint": "Please attach JSON code for dataset, linked service and screen shots to help us triage your problem faster",
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Please briefly describe the issue",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Is it a new issue or regression?"
                },
                {
                    "text": "Is the issue intermittent or persistent?"
                }
            ]
        },
        {
            "id": "error_message",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What error message do you see?",
            "required": false
        },
        {
            "id": "problem_report_id",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Is this a run time issue? If yes, please provide the Report ID from all nodes separated with commas. (see Solutions tab for guidance on how to obtain Report ID)"",
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate time when the problem stopped occurring. If the issue is ongoing, leave this field blank",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
