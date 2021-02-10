<properties
	pageTitle="Cloud App Security - Alerts and Investigation - Investigating activities"
	description="Cloud App Security - Alerts and Investigation - Investigating activities"
	authors="ms-nagrand"
	ms.author="nagrand"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32728980"
    productPesIds="16031"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_MCAS_Investigating activities"
	schemaVersion="1"
	ownershipId="CloudAppSecurity_API"
/>
# Alerts and Investigation - Investigating activities
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Alerts and Investigation - Investigating activities",
				"fileAttachmentHint": "1. Please attach the raw data of the activity from MCAS activity log. You can locate it under Investigate - Activity Log - Expand the activity - Source - View raw data 2. Please attach the correlated activity log from the source app. For example, for O365 apps (EXO, SPO, OD, etc.), please export the relevant log from https://protection.office.com/unifiedauditlog O365 Unified Audit logs",
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
                    "id": "issue_description",
                    "order": 3,
                    "controlType": "dropdown",
                    "displayLabel": "Please scope the issue that you're facing:",
                    "watermarkText": "Choose an option",
                    "dropdownOptions":
					[
                        {
                            "value": "Missing activities",
                            "text": "Missing activities"
                        },
                        {
                            "value": "Delayed activities/alerts",
                            "text": "Delayed activities/alerts"
                        },
                        {
                            "value": "Request more information about activity",
                            "text": "Request more information about activity"
                        },
						{
                            "value": "Incurracte activity field",
                            "text": "Incurracte activity field"
                        },
                        {
                            "value": "dont_know_answer",
                            "text": "Other"
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
