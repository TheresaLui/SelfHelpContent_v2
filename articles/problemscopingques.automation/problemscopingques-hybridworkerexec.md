<properties
	articleId="problemscopingques-hybridworkerexec.md"
	pageTitle="Azure Automation - Hybrid Worker"
	description="Azure Automation - Hybrid Worker"
	authors="zjalexander"
	ms.author="zachal"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32628014,32599940"
	productPesIds="15607"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_Automation"
/>
# Hybrid Worker
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Hybrid Worker",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "NodeName",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Please provide the computer name of the hybrid worker",
            "required": false
        },
        {
            "id": "runbook selection",
            "order": 2,
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
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "previously successful",
            "order": 4,
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
        }
    ],
    "$schema": "SelfHelpContent"
}
---
