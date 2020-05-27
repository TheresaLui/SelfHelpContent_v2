<properties
    pageTitle="ExpressRoute\Configuration and Setup\Tool Issues"
    description="ExpressRoute\Configuration and Setup\Tool Issues"
    authors="v-miegge"
    ms.author="v-miegge"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32627980"
    productPesIds="15480"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="8ceebecc-8b7d-43a0-b137-77b1cf98bb70"
	ownershipId="CloudNet_AzureExpressRoute"
/>
# Which tool(s) are you experiencing issues with?

---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
  "title": "Which tool(s) are you experiencing issues with?",
  "fileAttachmentHint": "",
  "formElements": [{
      "id": "slow_vm_determination",
      "order": 1,
      "controlType": "multiselectdropdown",
      "displayLabel": "Which tool(s) are you experiencing issues with?",
      "watermarkText": "Choose an option",
      "dropdownOptions": [{
          "value": "Portal",
          "text": "Portal"
        },
        {
          "value": "PowerShell",
          "text": "PowerShell"
        },
        {
          "value": "CLI",
          "text": "CLI"
        }
      ],
      "required": false
    },
    {
      "id": "problem_start_time",
      "order": 2,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem begin?",
      "required": true
    },
    {
      "id": "problem_description",
      "order": 5,
      "controlType": "multilinetextbox",
      "displayLabel": "Details",
      "watermarkText": "Provide additional information about your issue",
      "required": true,
      "useAsAdditionalDetails": true,
      "hints": [{
          "text": "Issue description."
        },
        {
          "text": "Describe the issue here."
        }
      ]
    }
  ]
}
---
