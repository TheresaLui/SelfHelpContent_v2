<properties
	articleId="problemscopingques-startop.md"
	pageTitle="Azure Automation - Start Stop VMs"
	description="Azure Automation - Start Stop VMs"
	authors="zjalexander"
	ms.author="zachal"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32615221,32615222,32615223,32635008,32635013,32635014,32635016"
	productPesIds="15607"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_Automation"
/>
# Automation Account
---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "Automation Account",
    "fileAttachmentHint": "Please provide a screenshot of any errors",
    "formElements": [
        {
            "id": "solutionOrScript",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Are you using the Start Stop Solution, or a custom script?",
            "dropdownOptions": [
                {
                    "value": "Solution",
                    "text": "I am using the Start-Stop VM Solution"
                },
                {
                    "value": "customScript",
                    "text": "I am using a script I wrote myself"
                },
                {
                    "value": "galleryScript",
                    "text": "I am using a script from the Runbook Gallery"
                }
            ],
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 10,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 30,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Describe the issue, including as much detail as possible with the exact text of error messages where available",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Include the exact text of any error messages that occur"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
