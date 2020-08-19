<properties 
  pageTitle="Network latency"
  description="Network latency"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740087"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="8120752b-92be-4243-af8f-4cb1da887968"
  ownershipId="AzureData_AzureSQLVM"
/>
# Network latency
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Network latency",
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
