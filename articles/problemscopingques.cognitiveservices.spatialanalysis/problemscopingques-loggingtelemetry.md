<properties
  pageTitle="Scoping questions - Issues related to spatial analysis usage"
  description="Scoping questions to troubleshoot the issues related to the system health, logging, and telemetry for spatial analysis."
  ms.author="kabrow"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32767691"
  productPesIds="16970"
  cloudEnvironments="public, Fairfax, usnat, ussec, mooncake"
  schemaVersion="1"
   articleId="7cd25d42-87e8-b2c6-92db-43555e41c55c"
  ownershipId="AzureCogSvc_CognitiveServices"
/>
# Issues related to the sytem health, telemetry, and logging for spatial analysis
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
  "title": "Issues related to the camera placement and configuration for the use of the spatial analysis container",
  "fileAttachmentHint": "Please provide a screenshot of any errors",
  "formElements": [{
      "id": "problem_start_time",
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem begin?",
      "required": true
    },{
      "id": "spatial_analysis_telegraf",
      "order": 2,
      "controlType": "multilinetextbox",
      "displayLabel": "Have you deployed the spatial-analysis-telegraf container? If so, what version?",
      "required": false
    },{
      "id": "spatial_analysis_diagnostics",
      "order": 3,
      "controlType": "multilinetextbox",
      "displayLabel": "Have you deployed the spatial-analysis-diagnostics container? If so, what version?",
      "required": false
    },{
      "id": "logging_information",
      "order": 4,
      "controlType": "multilinetextbox",
      "displayLabel": "Have you retrieved any logging information? If so, post below.",
      "required": false
    },{
      "id": "problem_description",
      "order": 5,
      "controlType": "multilinetextbox",
      "displayLabel": "Can you provide any additional details about the issue you are having regarding your container deployment?",
      "useAsAdditionalDetails": true,
      "required": true
    }
  ]
}
---
