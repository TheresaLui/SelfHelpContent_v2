<properties
    pageTitle="ExpressRoute or Connectivity Issues detected by NPM"
    description="ExpressRoute or Connectivity Issues detected by NPM"
    authors="v-miegge"
    ms.author="v-miegge,mariliu"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32602123"
    productPesIds="15480"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="1cefc7d8-95c4-3000-b8d3-487e67c13690"
	ownershipId="CloudNet_AzureExpressRoute"
/>
# Provide additional IP address information about your issue

---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
  "title": "VM Information",
  "fileAttachmentHint": "",
  "formElements": [{
      "id": "destination_vm internal IP address",
      "order": 1,
      "controlType": "textbox",
      "displayLabel": "Source IP Address(es)",
      "watermarkText": "Enter the Source IP address"
        },
        {
          "id": "resource internal IP address",
          "order": 2,
          "controlType": "textbox",
          "displayLabel": "Destination IP Address(es)",
          "watermarkText": "Enter the Destination IP address",
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
    }
---
