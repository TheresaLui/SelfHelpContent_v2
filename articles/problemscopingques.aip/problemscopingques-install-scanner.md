<properties
	pageTitle="Azure Information Protection - Installing, Onboarding, or Decommissioning - AIP Scanner Installation and Configuration"
	description="Azure Information Protection - Installing, Onboarding, or Decommissioning - AIP Scanner Installation and Configuration"
	authors="orbarak-ms"
	ms.author="orbarak"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32727933"
    productPesIds="14997"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_installation_issues_scanner"
	schemaVersion="1"
	ownershipId="AzureIdentity_InformationProtection"
/>
# Can't apply this label
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "AIP Scanner Installation and Configuration",
				"subscriptionRequired": false,
                "fileAttachmentHint": "Navigate to %temp% and include MSI installer logs",
                "formElements": [
                {
                    "id": "client_type",
                    "order": 2,
                    "controlType": "dropdown",
                    "displayLabel": "Which AIP Scanner did you try to install?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Azure Information Protection client (classic)",
                            "text": "Azure Information Protection client (classic)"
                        },
                        {
                            "value": "Azure Information Protection Unified Labeling Client",
                            "text": "Azure Information Protection Unified Labeling Client"
                        },
	                    {
							"value": "dont_know_answer",
							"text": "I don't know"
						}
                    ],
                    "required": true
                },{
                "id": "version_number",
                "order": 3,
				"visibility": "client_type == Azure Information Protection client (classic)",
                "controlType": "textbox",
                "displayLabel": "Which version are you using? For details, use the link in the help balloon",
				"infoBalloonText": "You can see the version number Using Protect/Sensitivity button - Help and Feedback. Verify that you use a <a href='https://docs.microsoft.com/azure/information-protection/rms-client/client-version-release-history'>supported version</a>",
                "required": true
                },{
                "id": "version_number_ul",
                "order": 4,
				"visibility": "client_type == Azure Information Protection Unified Labeling Client",
                "controlType": "textbox",
                "displayLabel": "Which version are you using? For details, use the link in the help balloon",
				"infoBalloonText": "You can see the version number Using Protect/Sensitivity button - Help and Feedback. Verify that you use a <a href='https://docs.microsoft.com/azure/information-protection/rms-client/unifiedlabelingclient-version-release-history'>supported version</a>",
                "required": true
                },{
                "id": "os_type",
                "order": 5,
                "visibility": "client_type == Azure Information Protection Unified Labeling Client",
                "controlType": "textbox",
                "displayLabel": "What Windows version are you using?",
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
