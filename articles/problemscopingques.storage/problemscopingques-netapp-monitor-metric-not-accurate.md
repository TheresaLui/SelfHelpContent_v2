<properties
	articleId="metric-not-accurate"
	pageTitle="Metric are not accurate or not populating"
	description="Metric are not accurate or not populating"
	authors="b-tonya"
	ms.author="b-tonya"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32740763"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Metric are not accurate or not populating
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
  "title": "Metric are not accurate or not populating",
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
      "displayLabel": "What interface(s) are you having issue with inaccurate metrics or not populating?",
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
      "id": "MetricType",
      "order": 3,
      "controlType": "dropdown",
      "displayLabel": "Are you having issue with Capacity Pool or Volume metric(s)?",
      "watermarkText": "",
      "dropdownOptions": [
        {
          "value": "Capacity_Pool_Metric",
          "text": "Capacity Pool Metric"
        },
        {
          "value": "Volume_Metric",
          "text": "Volume Metric"
        },
        {
          "value": "CapacityPool_Volume Metric",
          "text": "Capacity Pool and Volume Metric(s)"
        },
        {
          "value": "dont_know_answer",
          "text": "None of the above"
        }
      ],
      "required": true
    },
    {
      "id": "CapacityPoolMetric",
      "order": 4,
      "visibility": "MetricType == Capacity_Pool_Metric || MetricType == CapacityPool_Volume Metric",
      "controlType": "multilinetextbox",
      "displayLabel": "List the Capacity Pool metric(s) that you need help with?",
      "watermarkText": "(i.e. Pool Allocated Size, Pool Allocated Throughput, etc)",
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