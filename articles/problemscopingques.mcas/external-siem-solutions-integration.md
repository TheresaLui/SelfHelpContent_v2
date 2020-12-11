<properties
	pageTitle="Cloud App Security - Integrations with MCAS -  External SIEM solutions integration"
	description="Cloud App Security - Integrations with MCAS -  External SIEM solutions integration"
	authors="ms-nagrand"
	ms.author="nagrand"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32728977"
    productPesIds="16031"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_External SIEM solutions integration"
	schemaVersion="1"
	ownershipId="CloudAppSecurity_API"
/>
# Integrations with MCAS -  External SIEM solutions integration
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Integrations with MCAS -  External SIEM solutions integration",
				"fileAttachmentHint": "Please attach the SIEM Agent log, with the timestamp that's correlates the issue",
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
                    "id": "SIEM_Server",
                    "order": 3,
                    "controlType": "textbox",
                    "displayLabel": "What type of SIEM server you're trying to connect to?",
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
