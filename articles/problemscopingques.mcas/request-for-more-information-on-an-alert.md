<properties
	pageTitle="Cloud App Security - Alerts and Investigation - Request for more information on an alert"
	description="Cloud App Security - Alerts and Investigation - Request for more information on an alert"
	authors="ms-nagrand"
	ms.author="nagrand"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32729000"
    productPesIds="16031"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_MCAS_Request for more information on an alert"
	schemaVersion="1"
	ownershipId="CloudAppSecurity_DataScience"
/>
# Alerts and Investigation - Request for more information on an alert
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Alerts and Investigation - Request for more information on an alert",
				"fileAttachmentHint": "Please attach a screenshot of the alert",
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
                    "id": "alert_ID",
                    "order": 3,
                    "controlType": "textbox",
                    "displayLabel": "Please provide the alert ID. You can find it from the URL of the alert itself",
                    "required": false
				},
				{
                    "id": "SPO_OD_URL",
                    "order": 4,
                    "controlType": "textbox",
                    "displayLabel": "In case there's an activity which correlates the alert, please provide the event ID of the activity",
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
