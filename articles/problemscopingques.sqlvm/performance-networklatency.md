<properties 
    pageTitle="performance/network latency"
    description="performance/network latency"
    authors="vadeveka"
    ms.author="vadeveka"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32633512"
    productPesIds="14745"
    cloudEnvironments="public,fairfax"
    schemaVersion="1"
    articleId="5A4FFD6F-53C2-43F0-9EF3-E63C2A42F285"
	ownershipId="AzureData_AzureSQLVM"
/>
# performance/network latency
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "performance/network latency",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Start time of most recent occurrence",
            "required": true
        },
        {
            "id": "perf_current",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is the problem occurring right now?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        },
        {
            "id": "perf_detect",
            "order": 3,
            "controlType": "multiselectdropdown",
            "displayLabel": "How did you detect the network issue?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Iperf",
                    "text": "Iperf"
                },
                {
                    "value": "Azure Monitoring Alerts",
                    "text": "Azure Monitoring Alerts"
                },
                {
                    "value": "Other Monitoring tools (describe below)",
                    "text": "Other Monitoring tools (describe below)"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
