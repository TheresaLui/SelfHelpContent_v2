<properties
	pageTitle="Cloud App Security - Configuring Policy and Controls - Shadow IT and app discovery policies"
	description="Cloud App Security - Configuring Policy and Controls - Shadow IT and app discovery policies"
	authors="ms-nagrand"
	ms.author="nagrand"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32729003"
    productPesIds="16031"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_Shadow IT and app discovery policies"
	schemaVersion="1"
	ownershipId="CloudAppSecurity_Discovery"
/>
# Configuring Policy and Controls - Shadow_IT and app discovery policies
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Configuring Policy and Controls - Shadow IT and app discovery policies",
				"fileAttachmentHint": "Please attach a screenshot of the policy configuration",
				"subscriptionRequired": false,
                "formElements": [
                {
                    "id": "MCAS_URL",
                    "order": 2,
                    "controlType": "textbox",
                    "displayLabel": "Provide your MCAS tenant URL (e.g., https://(domain name).portal.cloudappsecurity.com/)",
                    "required": true
                },
				{
                    "id": "Policy_ID",
                    "order": 3,
                    "controlType": "textbox",
                    "displayLabel": "Provide the Policy ID by extracting it from the policy URL",
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
