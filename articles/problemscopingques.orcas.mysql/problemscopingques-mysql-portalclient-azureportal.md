<properties
    pageTitle="Portal, Client Tools and APIs"
    description="Portal, Client Tools and APIs"
    authors="Hang-Zhang"
    ms.author="haz"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32640048"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-mysql-toolsapis-azure_portal"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Portal, Client Tools and APIs - Azure Portal
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Tools and APIs Azure Portal",
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
            "id": "similar_issue_azure",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Have you encountered similar issues for other Azure resources (example Azure VM or Storage)?",
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
                    "text": "Don't know or unsure"
                }
            ],
            "required": false
        },
        {
            "id": "similar_issue_browser",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "If you have multiple web browsers, have you encountered similar issues in a different browser?",
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
                    "text": "Don't know or unsure"
                }
            ],
            "required": false
        },
        {
            "id": "similar_issue_computer",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "If you have multiple computers, have you encountered similar issues on other computers?",
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
                    "text": "Don't know or unsure"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Problem description",
            "watermarkText": "Provide your repro steps and other information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
