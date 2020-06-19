<properties 
  pageTitle="Virtual machine slow, unresponsive"
  description="Virtual machine slow, unresponsive"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740113"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="0a67af2f-e0fb-43f0-b653-8e158ed1d199"
  ownershipId="AzureData_AzureSQLVM"
/>
# Virtual machine slow, unresponsive
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Virtual machine slow, unresponsive",
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
            "id": "perf_constraints",
            "order": 3,
            "controlType": "multiselectdropdown",
            "displayLabel": "Which category of resource constraints did you observe?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "CPU",
                    "text": "CPU"
                },
                {
                    "value": "Memory",
                    "text": "Memory"
                },
                {
                    "value": "Disk",
                    "text": "Disk"
                },
                {
                    "value": "Network",
                    "text": "Network"
                }
            ],
            "required": false
        },
        {
            "id": "perf_detect",
            "order": 4,
            "controlType": "multiselectdropdown",
            "displayLabel": "How did you detect the resource constraint?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Perf Insights",
                    "text": "Perf Insights"
                },
                {
                    "value": "Iperf",
                    "text": "Iperf"
                },
                {
                    "value": "Azure Monitoring Alerts",
                    "text": "Azure Monitoring Alerts"
                },
                {
                    "value": "DiskSPD",
                    "text": "DiskSPD"
                },
                {
                    "value": "IOmeter",
                    "text": "IOmeter"
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
