<properties
	pageTitle="Cloud App Security - Configuring Policy and Controls - OAuth apps policies"
	description="Cloud App Security - Configuring Policy and Controls - OAuth apps policies"
	authors="ms-nagrand"
	ms.author="nagrand"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32728998"
    productPesIds="16031"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_OAuth apps policies"
	schemaVersion="1"
	ownershipId="CloudAppSecurity_API"
/>
# Configuring Policy and Controls - OAuth apps policies
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Configuring Policy and Controls - OAuth apps policies",
				"fileAttachmentHint": "1. Please attach a screenshot of the policy configuration 2. "Please provide a screenshot of the OAuth app page",
				"subscriptionRequired": false,
                "formElements": [
                {
                    "id": "MCAS_URL",
                    "order": 2,
                    "controlType": "textbox",
                    "displayLabel": "Please provide your MCAS tenant URL (e.g: https://(domain name).portal.cloudappsecurity.com/)",
                    "required": true
                },
				{
                    "id": "Policy_ID",
                    "order": 3,
                    "controlType": "textbox",
                    "displayLabel": "Please provide the Policy ID. The ID can be extracted from the policy URL",
                    "required": false
				},
				{
                    "id": "problem_description",
                    "order": 1,
                    "controlType": "multilinetextbox",
                    "displayLabel": "Description",
                    "useAsAdditionalDetails": true,
                    "required": true
                    },{
                    "id": "problem_start_time",
                    "order": 8,
                    "controlType": "datetimepicker",
                    "displayLabel": "When did the problem start?",
                    "required": true
                  }
                  ]
}
---
