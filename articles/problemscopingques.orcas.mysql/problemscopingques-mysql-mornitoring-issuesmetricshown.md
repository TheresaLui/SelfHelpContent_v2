<properties
    pageTitle="Monitoring and Alerting"
    description="Monitoring and Alerting"
    authors="Hang-Zhang"
    ms.author="haz"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32640063"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax"
    schemaVersion="1"
    articleId="problemscopingques-mysql-monitoring-issues_metricshown"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Monitoring and Alerting - Issues with metrics shown in the portal
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Monitoring Issues with metrics",
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
            "id": "metrics_issue",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Which metric(s) are you experiencing issues viewing?",
            "required": false
        },
        {
            "id": "experience_same_issue",
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
                    "value": "dont_know_answer",
                    "text": "Don't know or unsure"
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
