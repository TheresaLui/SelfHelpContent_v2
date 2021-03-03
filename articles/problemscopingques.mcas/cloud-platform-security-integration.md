<properties
	pageTitle="Cloud App Security - Integrations with MCAS -  Cloud platform security integration"
	description="Cloud App Security - Integrations with MCAS -  Cloud platform security integration"
	authors="ms-nagrand"
	ms.author="nagrand"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32728965"
    productPesIds="16031"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_Cloud platform security integration"
	schemaVersion="1"
	ownershipId="CloudAppSecurity_Portal"
/>
# Integrations with MCAS -  Cloud platform security integration
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Integrations with MCAS -  Cloud platform security integration",
				"fileAttachmentHint": "Please add a screenshot of the relevant Security configuration page",
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
