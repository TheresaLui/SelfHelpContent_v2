
<properties
pageTitle="Grafana dashboards issue"
description="Grafana dashboards issue"
articleId="problemscopingques-grafana-dashboards-issue"
authors="neilghuman"
ms.author="neghuman"
selfHelpType="problemScopingQuestions"
supportTopicIds="32727884"
productPesIds="15725"
cloudEnvironments="public, BlackForest, Fairfax, MoonCake, usnat, ussec"
schemaVersion="1"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Grafana dashboards issue
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Grafana dashboards issue",
    "fileAttachmentHint": "If possible, please upload screenshots and any additional attachments which may help the support engineer troubleshoot your issue.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "type_of_issue",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What type of issue is occurring?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Visualization issue in Grafana",
                    "text": "Visualization issue in Grafana"
                },
                {
                    "value": "Data missing or incorrect in Grafana",
                    "text": "Data missing or incorrect in Grafana"
                },
                                {
                    "value": "Setting up the integration between Azure Monitor Logs and Grafana",
                    "text": "Setting up the integration between Azure Monitor Logs and Grafana"
                },
                                {
                    "value": "Timeout while retrieving the data from the Log Analytics workspace",
                    "text": "Timeout while retrieving the data from the Log Analytics workspace"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know / Not sure"
                }
            ],
            "required": true
        },
        {
            "id": "prevously_worked",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Has this previously worked?",
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
                    "text": "Don't know / Not sure"
                }
            ],
            "required": false
        },
        {
            "id": "users",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Is the issue happening to a single user or multiple users?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Single user",
                    "text": "Single user"
                },
                {
                    "value": "Multiple users",
                    "text": "Multiple users"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know / Not sure"
                }
            ],
            "required": true
        },
        {
            "id": "itermittent_or_consistant",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Is the issue intermittent or constant?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Itermittent",
                    "text": "Itermittent"
                },
                {
                    "value": "Consistant",
                    "text": "Consistant"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know / Not sure"
                }
            ],
            "required": false
        },
        {
            "id": "query_being_executed",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the query being executed?",
            "watermarkText": "Please enter the full query being executed to retrieve the data into Grafana",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 10,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Describe the issue, including as much detail as possible with the exact text of error messages where available. Please also add query time range of the query (if not defined directly on the query itself).",
            "required": true,
            "hints": []
        }
    ]
}
---
