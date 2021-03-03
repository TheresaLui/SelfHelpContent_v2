<properties
	pageTitle="Cloud App Security - Portal Usage and Configuration - Unable to log in"
	description="Cloud App Security - Portal Usage and Configuration - Unable to log in"
	authors="ms-nagrand"
	ms.author="nagrand"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32729005"
    productPesIds="16031"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_Unable to log in"
	schemaVersion="1"
	ownershipId="CloudAppSecurity_Portal"
/>
# Portal Usage and Configuration - Unable to log in
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Portal Usage and Configuration - Unable to log in",
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
                    "id": "Error_Correlation_ID",
                    "order": 3,
                    "controlType": "textbox",
                    "displayLabel": "Please add the correlation ID (raw data) of the error",
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
