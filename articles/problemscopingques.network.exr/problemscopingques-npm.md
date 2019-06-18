<properties
    pageTitle="ExpressRoute\Connectivity Issues detected by NPM"
    description="ExpressRoute\Connectivity Issues detected by NPM"
    authors="v-miegge"
    ms.author="v-miegge"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32602123"
    productPesIds="15480"
    cloudEnvironments="public"
    schemaVersion="1"
    articleId="1cefc7d8-95c4-3000-b8d3-487e67c13690"
/>
# Provide additional IP address information about your issue.

---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
  "title": "VM Information",
  "fileAttachmentHint": "",
  "formElements": [{
      "id": "destination_vm internal IP address",
      "order": 1,
      "controlType": "textbox",
      "infoBalloonText": "string",
      "displayLabel": "Please provide the internal IP address of the source VM",
      "watermarkText": "Enter IP address of the source VM",
        },
        {
          "id": "resource internal IP address",
          "order": 2,
          "controlType": "textbox",
          "displayLabel": "Please provide the internal IP address of the destination VM",
          "watermarkText": "Enter IP address of the destination VM",
          "required": false
        },
        {
          "id": "problem_description",
          "order": 999,
          "controlType": "multilinetextbox",
          "useAsAdditionalDetails": true,
          "displayLabel": "Additional details",
          "watermarkText": "Provide additional information about your issue",
          "required": true,
          "hints": []
        },
        {
          "id": "problem_start_time",
          "order": 1000,
          "controlType": "datetimepicker",
          "displayLabel": "Problem start time",
          "required": true
        }
      ],
      "required": true
    },
    {
      "id": "learn_more_text",
      "order": 6,
      "controlType": "infoblock",
      "content": "<a href='https://jsonlint.com/'>Use this JSON Checker</a> if you are receiving validation errors in your scoping question"
    }
  ]
}
---
