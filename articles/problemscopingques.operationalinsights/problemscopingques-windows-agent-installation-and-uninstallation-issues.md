<properties
	articleId="problemscopingques-windows-agent-installation-and-uninstallation-issues"
	pageTitle="Windows agent installation and uninstallation issues"
	description="Windows agent installation and uninstallation issues"
	authors="neilghuman"
	ms.author="neghuman"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745401"
	productPesIds="15725"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	schemaVersion="1"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Windows agent installation and uninstallation issues
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Windows agent installation and uninstallation issues",
    "fileAttachmentHint": "Please upload screenshots of any relevant details. Include any additional information that can help the support engineer troubleshoot your issue.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start happening?",
            "required": true
        },
        {
            "id": "notification_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Which type of issue is occurring?",
            "watermarkText": "Choose and issue type",
            "dropdownOptions": [
                {
                    "value": "Cannot install the agent",
                    "text": "Cannot install the agent"
                },
                {
                    "value": "Cannot uninstall the agent",
                    "text": "Cannot uninstall the agent"
                },
                {
                    "value": "Cannot enable&#47;install the extension",
                    "text": "Cannot enable&#47;install the extension"
                },
                                {
                    "value": "Cannot disable&#47;uninstall the extension",
                    "text": "Cannot disable&#47;uninstall the extension"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ],
            "required": true
        },
        {
            "id": "problem_frequency",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is the issue happening on a single machine or multiple machines?",
            "watermarkText": "Is the issue happening on a single machine or multiple machines?",
            "required": true,
            "dropdownOptions": [
                {
                    "value": "Single Azure Virtual machine",
                    "text": "Single Azure Virtual machine"
                },
                {
                    "value": "Single Non-Azure machine",
                    "text": "Single Non-Azure machine"
                },
                {
                    "value": "Multiple Azure Virtual machines",
                    "text": "Multiple Azure Virtual machines"
                },
                                {
                    "value": "Multiple Non-Azure Virtual machines",
                    "text": "Multiple Non-Azure Virtual machines"
                },
                                {
                    "value": "Multiple Azure Virtual machines and Non-Azure machines",
                    "text": "Multiple Azure Virtual machines and Non-Azure machines"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ]
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "What's the name of an impacted machine? If there are multiple, please include a few names.",
            "watermarkText": "What's the name of an impacted machine? If there are multiple, please include a few names.",
            "required": true,
            "useAsAdditionalDetails": false,
            "hints": [
                {
                    "text": "Enter the name of the machine(s)"
                }
            ]
        },
        {
            "id": "windowsver",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Which version(s) of Windows is are the impacted machine(s) running?",
            "watermarkText": "Enter the name windows version(s).",
            "required": true,
            "useAsAdditionalDetails": false

        },
        {
            "id": "additional_information",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe the issue, including as much detail as possible with the exact text of error messages where available.",
            "watermarkText": "Please include the exact text of any error message.",
            "required": false,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
