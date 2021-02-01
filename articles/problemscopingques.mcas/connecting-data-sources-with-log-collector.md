<properties
	pageTitle="Cloud App Security - Connecting Apps and Continuous Data - Connecting data sources with log collector"
	description="Cloud App Security - Connecting Apps and Continuous Data - Connecting data sources with log collector"
	authors="ms-nagrand"
	ms.author="nagrand"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32728969"
    productPesIds="16031"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_Connecting data sources with log collector"
	schemaVersion="1"
	ownershipId="CloudAppSecurity_Discovery"
/>
# Connecting Apps and Continuous Data - Connecting data sources with log collector
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Connecting Apps and Continuous Data - Connecting data sources with log collector",
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
                    "id": "Is_The_Log_Collector_Behind_Proxy",
                    "order": 4,
                    "controlType": "dropdown",
                    "displayLabel": "Is the Log-collector installed behind a Proxy?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions":
					[
                        {
                            "value": "Yes",
                            "text": "Yes"
                        },
                        {
                            "value": "No",
                            "text": "No"
                        },
                        {
                            "value": "dont_know_answer",
                            "text": "Not relevant"
                        }
                    ],
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
