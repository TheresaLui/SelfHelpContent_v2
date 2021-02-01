<properties
	pageTitle="Cloud App Security - Integrations with MCAS -  REST APIs"
	description="Cloud App Security - Integrations with MCAS -  REST APIs"
	authors="ms-nagrand"
	ms.author="nagrand"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32729001"
    productPesIds="16031"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_REST APIs"
	schemaVersion="1"
	ownershipId="CloudAppSecurity_API"
/>
# Integrations with MCAS - REST APIs
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Integrations with MCAS -  REST APIs",
				"fileAttachmentHint": "In case of query timeouts/errors, please attach the relevant query/script",
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
                    "id": "Type_Of_Data",
                    "order": 3,
                    "controlType": "textbox",
                    "displayLabel": "Please provide what type of data you are trying to retrieve, and what is the approximate amount of records.",
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
