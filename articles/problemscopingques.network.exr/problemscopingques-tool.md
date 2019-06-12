<properties
    pageTitle="ExpressRoute\Configuration and Setup\Tool Issues"
    description="ExpressRoute\Configuration and Setup\Tool Issues"
    authors="v-miegge"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32627980"
    productPesIds="15585"
    articleId="expressroute-configuration-setup-tool-issues"
    cloudEnvironments="public"
    schemaVersion="1"
    articleId="8ceebecc-8b7d-43a0-b137-77b1cf98bb70"
/>
# Which tool(s) are you experiencing issues with?

---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
  "title": "Which tool(s) are you experiencing issues with?",
  "fileAttachmentHint": "",
  "formElements": [{
      "id": "slow_vm_determination",
      "order": 1,
      "controlType": "dropdown",
      "infoBalloonText": "string",
      "displayLabel": "Which tool(s) are you experiencing issues with?",
      "watermarkText": "Choose an option",
      "dropdownOptions": [{
          "value": "Portal",
          "text": "Portal"
        }, {
          "value": "PowerShell",
          "text": "PowerShell"
        }, {
          "value": "CLI",
          "text": "CLI"
        }
      ],
      "required": false
    }, {
      "id": "problem_start_time",
      "order": 2,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem begin?",
      "required": true
    }, {
      "id": "problem_description",
      "order": 5,
      "controlType": "multilinetextbox",
      "displayLabel": "Details",
      "watermarkText": "Provide additional information about your issue",
      "required": true,
      "useAsAdditionalDetails": true,
      "hints": [{
          "text": "Issue description."
        }, {
          "text": "Describe the issue here."
        }
      ]
    }, {
      "id": "learn_more_text",
      "order": 6,
      "controlType": "infoblock",
      "content": "<a href='https://jsonlint.com/'>Use this JSON Checker</a> if you are receiving validation errors in your scoping question"
    }
  ]
}
---