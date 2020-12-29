<properties
  articleId="86d55dcb-dda4-c096-a850-ed79ec53140a"
  pageTitle="Scoping questions - Issues related to Anomaly Detector usage"
  description="Scoping questions to troubleshoot the issues related to usage of Anomaly Detector, inluding usage of SDK, Rest API, container."
  authors="zhli2"
  authoralias="zhli2"
  ms.author="zhli2"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740927"
  productPesIds="17253"
  cloudEnvironments="public, Fairfax, usnat, ussec, mooncake"
  schemaVersion="1"
  ownershipId="AzureCogSvc_CognitiveServices"
/>
# Issues related to Anomaly Detector usage
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
  "title": "Issues related to usage of Anomaly Detector",
  "fileAttachmentHint": "Please provide a screenshot of any errors",
  "formElements": [
    {
      "id": "problem_start_time",
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem begin?",
      "required": true
    },
    {
      "id": "usage_scenario",
      "order": 2,
      "controlType": "radiobuttongroup",
      "displayLabel": "How are you using Anomaly Detector?",
      "radioButtonOptions": [
        {
          "value": "SDK",
          "text": "Using SDK"
        },
        {
          "value": "restapi",
          "text": "Using Rest API"
        },
        {
          "value": "container",
          "text": "Using container"
        }
      ],
      "required": true
    },
    {
      "id": "problem_description",
      "order": 3,
      "controlType": "multilinetextbox",
      "displayLabel": "Problem description",
      "watermarkText": "Provide additional information about your issue",
      "useAsAdditionalDetails": true,
      "required": true
    }
  ]
}
---