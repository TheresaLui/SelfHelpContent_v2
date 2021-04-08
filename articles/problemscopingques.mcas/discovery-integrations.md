<properties
	pageTitle="Cloud App Security - Integrations with MCAS -  Discovery integrations"
	description="Cloud App Security - Integrations with MCAS -  Discovery integrations"
	authors="ms-nagrand"
	ms.author="nagrand"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32729007"
    productPesIds="16031"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_Discovery integrations"
	schemaVersion="1"
	ownershipId="CloudAppSecurity_Discovery"
/>
# Integrations with MCAS -  Discovery integrations
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Integrations with MCAS -  Discovery integrations",
				"fileAttachmentHint": "In case of pending tasks issue please attach an export of your governance log",
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
