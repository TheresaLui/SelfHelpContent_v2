<properties
	articleId="problemscopingques-updatemgmt.md"
	pageTitle="Azure Automation - Update Management"
	description="Azure Automation - Update Management"
	authors="zjalexander,summertgu"
	ms.author="zachal,tiag"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32599864,32615228,32599903,32615227,32599924,32615229,32599936,32599937,32633803,32633804,32642183,32642184,32642182,32642186,32642185,32642187,32642191"
	productPesIds="15607,14749,15571,15797,16454,16470"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_Automation"
/>
# Update Management
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Update Management",
    "fileAttachmentHint": "Please provide a screenshot of any errors",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 10,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "NodeName",
            "order": 20,
            "controlType": "textbox",
            "displayLabel": "Please provide the computer name of one or more affected machines",
            "required": false
        },
        {
            "id": "OperatingSystem",
            "order": 25,
            "controlType": "dropdown",
            "displayLabel": "What OS are the affected machines?",
            "dropdownOptions": [
                {
                    "value": "Windows",
                    "text": "Windows Server"
                },
                {
                    "value": "Linux",
                    "text": "Linux"
                },
                {
                    "value": "Both",
                    "text": "Both Windows and Linux"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 30,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Include the exact text of any error messages that occur"
                }
            ]
        },
        {
            "id": "learn_more_text",
            "order": 40,
            "controlType": "infoblock",
            "content": "<a href='https://docs.microsoft.com/azure/automation/troubleshoot/update-management'>Learn more</a> about troubleshooting Update Management"
        }
    ],
    "$schema": "SelfHelpContent"
}
---
