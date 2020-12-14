<properties
	pageTitle="Cloud App Security - Configuring Policy and Controls - DLP and file policies"
	description="Cloud App Security - Configuring Policy and Controls - DLP and file policies"
	authors="ms-nagrand"
	ms.author="nagrand"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32728974"
    productPesIds="16031"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_DLP and file policies"
	schemaVersion="1"
	ownershipId="CloudAppSecurity_DataProtection"
/>
# Configuring Policy and Controls - DLP and file policies
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Configuring Policy and Controls - DLP and file policies",
				"fileAttachmentHint": "1. Please attach a screenshot of the policy configuration 2. For Content inspection issues, please attach a screenshot of the Built-in-DLP/DCS configuration",
				"subscriptionRequired": false,
                "formElements": [
                {
                    "id": "MCAS_URL",
                    "order": 2,
                    "controlType": "textbox",
                    "displayLabel": "Please provide your MCAS tenant URL (e.g., https://(domain name).portal.cloudappsecurity.com/)",
                    "required": true
                },
				{
                    "id": "File_ID",
                    "order": 3,
                    "controlType": "textbox",
                    "displayLabel": "Provide the File ID from MCAS portal - Investigate - Files - Expand the file properties - View File Identifiers - Copy the File ID (if one exists)",
                    "required": false
				},
				{
                    "id": "Policy_ID",
                    "order": 4,
                    "controlType": "textbox",
                    "displayLabel": "Provide the Policy ID. The ID can be extracted from the policy URL.",
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
