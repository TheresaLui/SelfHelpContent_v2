
<properties
pageTitle="Service Map or Dependency agent"
description="Service Map or Dependency agent"
articleId="problemscopingques-Service_Map_or_Dependency_agent"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32745414"
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
schemaVersion="1"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Service Map or Dependency agent
---
{
    "resourceRequired": true,
    "title": "Service Map or Dependency agent",
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
            "id": "did_it_work",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is the issue related to the solution setup or agent installation?",
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
            "id": "error_message",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What error are you seeing?",
            "watermarkText": "Enter error message",
            "required": false
        },
        {
            "id": "affected_machine",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What's the name of an affected machine? If there are multiple, please include a few names",
            "watermarkText": "Enter the name of the machine(s)",
            "required": false
        },
        {
            "id": "os_name",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "What is the operating system of the affected machines?",
            "watermarkText": "Enter the operating system name",
            "required": false
        },
        {
            "id": "version_number",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "What are the versions for the log analytics and dependency agents?",
            "watermarkText": "Enter the agents versions",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 7,
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