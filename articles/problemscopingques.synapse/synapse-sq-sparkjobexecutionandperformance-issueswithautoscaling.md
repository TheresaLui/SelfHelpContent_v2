<properties
    schemaVersion = "1"
    selfHelpType = "problemScopingQuestions"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    productPesIds = "15818"
    supportTopicIds = "32783889"
    pageTitle = "Spark Job Execution and Performance/Issues with Autoscaling"
    description = "Spark Job Execution and Performance/Issues with Autoscaling"
    articleId = "synapse-sq-sparkjobexecutionandperformance-issueswithautoscaling.md"
    ms.author = "saltug"
/>

# Spark Job Execution and Performance/Issues with Autoscaling

---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "fileAttachmentHint": "",
    "title": "Issues with Autoscaling",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "required": true,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "infoBalloonText": ""
        },
        {
            "id": "language",
            "order": 2,
            "required": true,
            "controlType": "DropDown",
            "displayLabel": "Language?",
            "watermarkText": "",
            "infoBalloonText": "",
            "content": null,
            "dropdownOptions": [
                {
                    "text": "PySpark (Python)",
                    "value": "PySpark (Python)"
                },
                {
                    "text": "Spark (Scala)",
                    "value": "Spark (Scala)"
                },
                {
                    "text": ".NET Spark (C#)",
                    "value": ".NET Spark (C#)"
                },
                {
                    "text": "Spark SQL",
                    "value": "Spark SQL"
                }
            ]
        },
        {
            "id": "yarn_app_id",
            "order": 3,
            "required": false,
            "controlType": "textbox",
            "displayLabel": "What was the Yarn Application ID?",
            "watermarkText": "eg. application_123456789012_0001",
            "infoBalloonText": "You can find this info from Synapse Studio"
        },
        {
            "id": "livy_job_id",
            "order": 4,
            "required": false,
            "controlType": "textbox",
            "displayLabel": "What was the Livy Job ID?",
            "watermarkText": "",
            "infoBalloonText": "You can find this info from Synapse Studio"
        },
        {
            "id": "error_message",
            "order": 5,
            "required": false,
            "controlType": "textbox",
            "displayLabel": "If an error appeared, what was the message?",
            "watermarkText": "",
            "infoBalloonText": ""
        },
        {
            "id": "problem_description",
            "order": 6,
            "required": true,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "infoBalloonText": "",
            "useAsAdditionalDetails": true
        }
    ]
}
---


