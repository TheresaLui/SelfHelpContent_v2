<properties
    pageTitle="ExpressRoute\Connectivity Issues detected by NPM"
    description="ExpressRoute\Connectivity Issues detected by NPM"
    authors="v-miegge"
    ms.author="v-miegge"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32602122"
    productPesIds="15585"
    cloudEnvironments="public"
    schemaVersion="1"
    articleId="1cefc7d8-95c4-429c-b8d3-487e67c13690"
/>

# Provide additional IP address information about your issue.

---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
  "title": "Provide additional IP address information about your issue.",
  "fileAttachmentHint": "",
  "formElements": [{
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
					"text": "Source IP Address(es)"
				},
				{
					"text": "Include all source IP addresses."
				}
				{
					"text": "Destination IP Address(es)"
				},
				{
					"text": "Include all destination IP addresses."
				}
			]
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
