<properties
	pageTitle="Cloud App Security - Connecting Apps and Continuous Data - Data sources formats and parsing"
	description="Cloud App Security - Connecting Apps and Continuous Data - Data sources formats and parsing"
	authors="ms-nagrand"
	ms.author="nagrand"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32728972"
    productPesIds="16031"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_Data sources formats and parsing"
	schemaVersion="1"
	ownershipId="CloudAppSecurity_Discovery"
/>
# Connecting Apps and Continuous Data - Data sources formats and parsing
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Connecting Apps and Continuous Data - Data sources formats and parsing",
				"fileAttachmentHint": "For data parsing issues, please upload an example of your traffic log",
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
                    "id": "OS_version_Data_Source",
                    "order": 3,
                    "controlType": "textbox",
                    "displayLabel": "Please add the OS and version of the data source",
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
