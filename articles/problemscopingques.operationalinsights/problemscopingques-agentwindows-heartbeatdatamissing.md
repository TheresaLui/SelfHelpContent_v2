<properties
pageTitle="Agent not reporting data or Heartbeat data missing"
description="Agent not reporting data or Heartbeat data missing"
articleId="problemscopingques-Windows_Agent not reporting data or Heartbeat data missing"
authors="yossiy,luki,shemers"
ms.author="yossiy,luki,shemers"
selfHelpType="problemScopingQuestions"
supportTopicIds="32612463"
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
schemaVersion="1"
ownershipId="AzureMonitoring_LogAnalytics"
/>

# Agent not reporting data or Heartbeat data missing
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Agent not reporting data or Heartbeat data missing",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": false
        },
        {
            "id": "single_multiple_machines",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is the issue on a single machine or multiple machines?",
            "watermarkText": "Choose an option",
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
                    "value": "Multiple Non-Azure machines",
                    "text": "Multiple Non-Azure machines"
                },
                {
                    "value": "Multiple Azure Virtual machines and Non-Azure machines",
                    "text": "Multiple Azure Virtual machines and Non-Azure machines"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not sure"
                }
            ],
            "required": true
        },
          {
            "id": "virtualmachine_id",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Please select affected virtual machine name.",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/providers/Microsoft.Compute/virtualMachines?api-version=2018-10-01",
               "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
            "dropdownOptions": [
                {
                    "value": "Unable to get the list of virtual machines",
                    "text": "Unable to get the list of virtual machines"
                }
            ],
            "required": false
        },
        {
            "id": "affected_machine",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "If any of the affected machine is a non-Azure machine, please type the machine(s) name",
            "watermarkText": "Enter the name of the machine(s)",
            "required": false
        },
        {
            "id": "is_troubleshooting",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Have you tried to execute the agent troubleshooting tool to fix this problem?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not sure"
                }
            ],
            "required": true
        },
        {
            "id": "missing_data",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "	5. What data is missing?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "All data, including heartbeat",
                    "text": "All data, including heartbeat"
                },
                {
                    "value": "Only heartbeat data",
                    "text": "Only heartbeat data"
                },
                {
                    "value": "Just some data type(s)",
                    "text": "Just some data type(s)"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not sure"
                }
            ],
            "required": true
        },
        {
            "id": "error_message",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "What version of Windows are you running?",
            "watermarkText": "Enter the Windows version",
            "required": false
        },
        {
            "id": "win_version",
            "order": 8,
            "controlType": "textbox",
            "displayLabel": "What version of Windows are you running?",
            "watermarkText": "Enter the Windows version",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 9,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Describe the issue, including as much detail as possible with the exact text of error messages where available. If only some data type(s) are missing, please specify which one(s).",
            "required": true,
            "hints": [
                {
                    "text": "Please provide a screenshot of any errors. In case you’re using an ARM template, please also attach all relevant JSON files."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---