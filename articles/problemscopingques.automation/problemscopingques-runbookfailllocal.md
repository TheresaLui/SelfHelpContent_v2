<properties
	articleId="problemscopingques-runbookfaillocal.md"
	pageTitle="Azure Automation - Runbook Execution"
	description="Azure Automation - Runbook Execution"
	authors="zjalexander"
	ms.author="zachal"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32635012"
	productPesIds="15607"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_Automation"
/>
# Runbook Execution
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Runbook failure",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "runbook selection",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Select the runbook that has the problem",
            "watermarkText": "Choose a runbook",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.Automation/automationAccounts/{resourcename}/runbooks?api-version=2017-05-15-preview",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "previously successful",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Has this runbook successfully run in Azure Automation before?",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes, this runbook has successfully run in Azure Automation before"
                },
                {
                    "value": "No",
                    "text": "No, this runbook has never successfully run in Azure Automation"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Paste in the exact text of any errors that occurred."
                }
            ]
        },
        {
            "id": "learn_more_text",
            "order": 6,
            "controlType": "infoblock",
            "content": "<a href='https://docs.microsoft.com//azure/automation/troubleshoot/runbooks'>Learn more</a> about troubleshooting runbooks"
        }
    ],
    "$schema": "SelfHelpContent"
}
---
