<properties
	pageTitle="Azure Information Protection - Installing, Onboarding, or Decommissioning - Migration from AIP to Unified Labeling - SCC"
	description="Azure Information Protection - Installing, Onboarding, or Decommissioning - Migration from AIP to Unified Labeling - SCC"
	authors="orbarak-ms"
	ms.author="orbarak"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32727950"
    productPesIds="14997"
	cloudEnvironments="public, blackForest, mooncake, fairfax"
    articleId="scoping_installation_migration_scc"
	schemaVersion="1"
	ownershipId="AzureIdentity_InformationProtection"
/>
# Can't apply this label
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Migration from AIP to Unified Labeling - SCC",
				"subscriptionRequired": false,
                "fileAttachmentHint": "Provide screenshot of the error seen in the portal",
                "formElements": [
                {
                    "id": "portal_type",
                    "order": 2,
                    "controlType": "dropdown",
                    "displayLabel": "Which portal are you using?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "AIP Portal",
                            "text": "AIP Portal"
                        },
                        {
                            "value": "SCC Portal",
                            "text": "SCC Portal"
                        },
	                    {
							"value": "dont_know_answer",
							"text": "I don't know"
						}
                    ],
                    "required": true
                },{
                    "id": "sccmigrate",
                    "order": 5,
                    "controlType": "dropdown",
                    "displayLabel": "Did you activate Unified Labeling in your tenant?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Yes",
                            "text": "Yes"
                        },
                        {
                            "value": "No",
                            "text": "No"
                        }
                    ],
                    "required": false
                },{
                    "id": "publishlabels",
                    "order": 6,
                    "visibility": "sccmigrate == Yes",
                    "controlType": "dropdown",
                    "displayLabel": "Did you publish labels in the SCC portal?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Yes",
                            "text": "Yes"
                        },
                        {
                            "value": "No",
                            "text": "No"
                        }
                    ],
                    "required": false
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
