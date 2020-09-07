<properties
    pageTitle="Scoping questions for process server deployment and issues"
    description="Scoping questions for process server deployment and issues"
    authors="TobyTu"
    ms.author="aaronmax"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32536429"
    productPesIds="16370"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="2b342a85-2019-4b4d-b7d0-43639892e013"
	ownershipId="Compute_SiteRecovery"
/>
# Questions Process Server Deployment and Issues
---
{
  "subscriptionRequired": true,
  "resourceRequired": true,
	"title": "Process Server Deployment and Issues",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "ServerName_ErrorID",
			"order": 1,
			"controlType": "textbox",
			"displayLabel": "Provide name of the process server (or) error Id:",
			"watermarkText": "Enter the name of the affected process server or error code",
			"required": false
		}, {
			"id": "problem_start_time",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
            "id": "Select_Error",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": " I have an issue with:",
            "watermarkText": "Choose an issue",
            "dropdownOptions": [
                {
                    "value": "My process server health is critical",
                    "text": "My process server health is critical"
                },
                {
                    "value": "My process server is in a warning state",
                    "text": "My process server is in a warning state"
                },
                {
                    "value": "Scale-out process server deployment has failed",
                    "text": "Scale-out process server deployment has failed"
                },
                {
                    "value": "My process server CPU utilization or memory usage is high, free space is low",
                    "text": "My process server CPU utilization or memory usage is high, free space is low"
                }
            ],
            "required": false
        }, {
			"id": "Basic_troubleshooting_multiselect",
			"order": 4,
			"controlType": "multiselectdropdown",
			"displayLabel": "I have gone through these steps:",
			"dropdownOptions": [{
					"value": "I resolved process server health alerts",
					"text": "I resolved process server health alerts"
				}, {
					"value": "All process server services are in Running state",
					"text": "All process server services are in Running state"
				}, {
					"value": "Process server heartbeat is the latest",
					"text": "Process server heartbeat is the latest"
				}, {
					"value": "I resolved connectivity and replication errors",
					"text": "I resolved connectivity and replication errors"
				}, {
					"value": "Other, don't know or not applicable",
					"text": "Other, don't know or not applicable"
				}
			],
			"required": false
		}, {
			"id": "problem_description",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": []
		}
	],
  "$schema": "SelfHelpContent"
}
---