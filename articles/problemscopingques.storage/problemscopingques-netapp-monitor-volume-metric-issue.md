<properties
	articleId="volume-metric-issue"
	pageTitle="Volume metric issue"
	description="Volume metric issue"
	authors="b-tonya"
	ms.author="b-tonya"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32740778"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Volume metric issue
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
  "title": "Volume metric issue",
  "fileAttachmentHint": "",
  "formElements": [
    {
      "id": "problem_start_time",
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem start?",
      "required": true
    },
    {
      "id": "InterfaceUsed",
      "order": 2,
      "controlType": "dropdown",
      "displayLabel": "What are the interface(s) where you are having issues with the volume metrics?",
      "watermarkText": "(i.e. Portal, REST API, CLI)",
      "dropdownOptions": [
        {
          "value": "Portal",
          "text": "Portal"
        },
        {
          "value": "REST API",
          "text": "REST API"
        },
        {
          "value": "PowerShell or CLI",
          "text": "CLI"
        },
        {
          "value": "All intefaces",
          "text": "All interfaces"
        },
        {
          "value": "dont_know_answer",
          "text": "None of the above"
        }
      ],
      "required": true
    },
    {
      "id": "VolumeMetric",
      "order": 5,
      "visibility": "MetricType == Volume_Metric || MetricType == CapacityPool_Volume Metric",
      "controlType": "multilinetextbox",
      "displayLabel": "List the Volume metric(s) that you need help with?",
      "watermarkText": "(i.e. Average Read Latency, Write Throughput, etc)",
      "required": true
    },
    {
      "id": "region",
      "order": 6,
      "controlType": "textbox",
      "displayLabel": "What location or region are you having issues with?",
      "watermarkText": "(i.e. Central US, North Europe, South India, ... or All locations)",
      "required": false
    },
    {
      "id": "problem_description",
      "order": 7,
      "controlType": "multilinetextbox",
      "displayLabel": "Provide any additional details",
      "required": true,
      "useAsAdditionalDetails": true
    },
    {
      "id": "error_message",
      "order": 8,
      "controlType": "textbox",
      "displayLabel": "Error message",
      "watermarkText": "What was the error message?",
      "required": false
    }
  ]
}
---