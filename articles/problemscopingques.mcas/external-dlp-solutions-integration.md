<properties
	pageTitle="Cloud App Security - Integrations with MCAS -  External DLP solutions integration"
	description="Cloud App Security - Integrations with MCAS -  External DLP solutions integration"
	authors="ms-nagrand"
	ms.author="nagrand"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32728976"
    productPesIds="16031"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_External DLP solutions integration"
	schemaVersion="1"
	ownershipId="CloudAppSecurity_DataProtection"
/>
# Integrations with MCAS -  External DLP solutions integration
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Integrations with MCAS -  External DLP solutions integration",
				"fileAttachmentHint": "Please add a screenshot of the External DLP connector status from MCAS portal",
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
                    "id": "ICAP_Version",
                    "order": 3,
                    "controlType": "textbox",
                    "displayLabel": "Please add the version of your ICAP server",
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
