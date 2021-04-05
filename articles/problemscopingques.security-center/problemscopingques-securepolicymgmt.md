<properties
	pageTitle="Azure Defender - Security Policy (built-in) management"
	description="Azure Defenderr - Security Policy (built-in) management"
	authors="orbarak-ms"
	ms.author="orbarak"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32788562"
    productPesIds="15947"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_asc_secpolmgmt"
	schemaVersion="1"
	ownershipId="Azure_Security_Security_Center"
/>
# Configuring Features and Resources - Just-in-time access (JIT)
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Security Policy (built-in) management",
				"fileAttachmentHint": "Upload the Resource Graph output in CSV using: securityresources | where type == 'microsoft.security/securescores' or type == 'microsoft.security/securescores/securescorecontrols'",
				"subscriptionRequired": false,
                "formElements": [
                {
                "id": "init_name",
                "order": 3,
                "controlType": "textbox",
                "displayLabel": "Specify the Recommendation or Policy name",
                "required": true
                },{
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
