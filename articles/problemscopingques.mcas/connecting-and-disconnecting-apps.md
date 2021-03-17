<properties
	pageTitle="Cloud App Security - Connecting Apps and Continuous Data - Connecting and disconnecting apps"
	description="Cloud App Security - Connecting Apps and Continuous Data - Connecting and disconnecting apps"
	authors="ms-nagrand"
	ms.author="nagrand"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32728968"
    productPesIds="16031"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_Connecting and disconnecting apps"
	schemaVersion="1"
	ownershipId="CloudAppSecurity_API"
/>
# Connecting Apps and Continuous Data - Connecting and disconnecting apps
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Connecting Apps and Continuous Data - Connecting and disconnecting apps",
				"fileAttachmentHint": "In case of an error in the connected app, please add a screenshot of it",
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
                    "id": "Error",
                    "order": 3,
                    "controlType": "textbox",
                    "displayLabel": "In case of error in Connected app, please add the error",
                    "required": false
				},
				{
                    "id": "App_name",
                    "order": 4,
                    "controlType": "textbox",
                    "displayLabel": "Please add the name of the connected/disconnected Instance, and its ID (The ID can be extracted from clicking the connected app - the ID will be in the app URL)",
                    "required": false
				},
				{
                    "id": "AAD_role_of_the_connecting_user",
                    "order": 5,
                    "controlType": "textbox",
                    "displayLabel": "In case of issues in connecting apps, please add the AAD role of the user that tries to connect the app",
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
