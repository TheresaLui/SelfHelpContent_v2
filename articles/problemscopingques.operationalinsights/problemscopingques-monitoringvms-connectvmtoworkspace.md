
<properties
pageTitle="Connect VM to workspace or no VM data in workspace"
description="Connect VM to workspace or no VM data in workspace"
articleId="problemscopingques-Connect_VM_to_workspace_or_no_VM_data_in_workspace"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32745397,32745398"
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
schemaVersion="1"
ownershipId="AzureMonitoring_LogAnalytics"
/>

# Connect VM to workspace or no VM data in workspace
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Connect VM to workspace or no VM data in workspace",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "single_multiple_machines",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is the issue on a single machine or multiple machines?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Single machine",
                    "text": "Single machine"
                },
                {
                    "value": "Multiple machines",
                    "text": "Multiple machines"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not sure"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "is_it_azure_vm",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is this an Azure VM?",
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
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "vm_os",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "What is the VM OS you are running (can be found under VM, Properties in Azure portal)?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Windows",
                    "text": "Windows"
                },
                {
                    "value": "Linux",
                    "text": "Linux"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not sure"
                }
            ],
            "required": false
        },
        {
            "id": "VM_version",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "What version of agent are you running? (can be found under VM, Properties in Azure portal)?",
            "watermarkText": "Enter VM agent version",
            "required": false
        },
        {
            "id": "error_message",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "What error are you seeing?",
            "watermarkText": "Enter the error message",
            "required": false
        },
        {
            "id": "affected_machine",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "What's the name of an affected machine? If there are multiple, please include a few names",
            "watermarkText": "Enter the name of the machine(s)",
            "required": false
        },
        {
            "id": "workspace_id",
            "order": 8,
            "controlType": "dropdown",
            "displayLabel": "Please select affected workspace name.",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/providers/Microsoft.OperationalInsights/workspaces?api-version=2015-11-01-preview",
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
                    "value": "Unable to get the list of Workspaces",
                    "text": "Unable to get the list of Workspaces"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 9,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        }
    ],
    "$schema": "SelfHelpContent"
}
---


