<properties
    pageTitle="Portal, Client Tools and APIs"
    description="Portal, Client Tools and APIs"
    authors="Hang-Zhang"
    ms.author="haz"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32640093"
    productPesIds="16221"
    cloudEnvironments="public"
    schemaVersion="1"
    articleId="problemscopingques-mysql-toolsapis-setup_alert"
/>
# Portal, Client Tools and APIs - Setting up Monitoring and Alerts
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Tools and APIs Setting Monitor Alerts",
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
            "id": "metric_issue",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Which metric(s) are you experiencing issues with?",
            "required": false
        },
        {
            "id": "same_issue_server",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "If you have multiple servers, did you experience the same issue on other servers?",
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
                    "value": "I don't have the answer",
                    "text": "I don't have the answer"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
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
