<properties
	pageTitle="Cloud App Security - Alerts and Investigation - Investigating files"
	description="Cloud App Security - Alerts and Investigation - Investigating files"
	authors="ms-nagrand"
	ms.author="nagrand"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32728982"
    productPesIds="16031"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_MCAS_Investigating files"
	schemaVersion="1"
	ownershipId="CloudAppSecurity_DataProtection"
/>
# Alerts and Investigation - Investigating files
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Alerts and Investigation - Investigating files",
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
                    "id": "File_ID",
                    "order": 3,
                    "controlType": "textbox",
                    "displayLabel": "Please provide the File ID from MCAS portal - Investigate - Files - Expand the file properties - View File Identifiers - Copy the File ID (if exist)",
                    "required": false
				},
				{
                    "id": "SPO_OD_URL",
                    "order": 4,
                    "controlType": "textbox",
                    "displayLabel": "If the file doesn't exist in MCAS, and the scenario related to SPO/OD, please preview the file in either of the services, and copy the URL",
                    "required": false
				},
				{
                    "id": "Activity_ID",
                    "order": 5,
                    "controlType": "textbox",
                    "displayLabel": "For Upload/Download/Access/rename/share scenarios, please provide the activity ID of the activity from MCAS activity log",
                    "required": false
				},
				{
                    "id": "Policy_ID",
                    "order": 6,
                    "controlType": "textbox",
                    "displayLabel": "If you have a policy that should match the file, provide policy ID. This can be extracted from the Policy URL",
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
