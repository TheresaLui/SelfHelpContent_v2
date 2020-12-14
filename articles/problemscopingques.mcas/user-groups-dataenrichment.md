<properties
	pageTitle="Cloud App Security - Portal Usage and Configuration - User groups data enrichment"
	description="Cloud App Security - Portal Usage and Configuration - User groups data enrichment"
	authors="ms-nagrand"
	ms.author="nagrand"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32729006"
    productPesIds="16031"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_User groups data enrichment"
	schemaVersion="1"
	ownershipId="CloudAppSecurity_Portal"
/>
# Portal Usage and Configuration - User groups data enrichment
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Portal Usage and Configuration - User groups data enrichment",
				"fileAttachmentHint": "Please add screenshots of the user groups, both from MCAS, and the source app (O365, Gsuite, etc.)",
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
