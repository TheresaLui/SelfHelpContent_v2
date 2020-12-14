<properties
	pageTitle="Cloud App Security - Portal Usage and Configuration - Investigating performance and latency issues"
	description="Cloud App Security - Portal Usage and Configuration - Investigating performance and latency issues"
	authors="ms-nagrand"
	ms.author="nagrand"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32728975"
    productPesIds="16031"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_Investigating performance and latency issues"
	schemaVersion="1"
	ownershipId="CloudAppSecurity_Portal"
/>
# Portal Usage and Configuration - Investigating_performance_and_latency_issues
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Portal Usage and Configuration - Investigating performance and latency issues",
				"fileAttachmentHint": "In case of query timeout in the portal, please add a screenshot decribing the query",
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
