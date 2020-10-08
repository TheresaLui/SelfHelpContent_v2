<properties
	pageTitle="Azure Defender - Data Collection - Workspaces"
	description="Azure Defender - Data Collection - Workspaces"
	authors="orbarak-ms"
	ms.author="orbarak"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32749431"
    productPesIds="15947"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_asc_datacollection_workspaces"
	schemaVersion="1"
	ownershipId="Azure_Security_Security_Center"
/>
# Data Collection - Workspaces
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Data Collection - Workspaces",
				"subscriptionRequired": false,
                "formElements": [
                {
                    "id": "prov_settings",
                    "order": 2,
                    "controlType": "dropdown",
                    "displayLabel": "What are your Auto Provisioning Settings?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "On",
                            "text": "On"
                        },
                        {
                            "value": "Off",
                            "text": "Off"
                        },
						{
                            "value": "dont_know_answer",
                            "text": "Don't know"
                        }
                    ],
                    "required": true
                },{
                    "id": "workspace_config",
                    "order": 3,
                    "controlType": "dropdown",
                    "displayLabel": "What is your Workspace Configuration?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Default ASC workspace",
                            "text": "Default ASC workspace"
                        },
                        {
                            "value": "User workspace",
                            "text": "User workspace (Provide Name/ID below)"
                        },
						{
                            "value": "dont_know_answer",
                            "text": "Don't know"
                        }
                    ],
                    "required": true
                },{
                "id": "user_workspace",
                "order": 4,
				"visibility": "workspace_config == User workspace",
                "controlType": "textbox",
                "displayLabel": "Please enter the Name/ID of your User Workspace",
                "required": false
                },{
                    "id": "defender_plan_settings",
                    "order": 5,
                    "controlType": "dropdown",
					"visibility": "workspace_config == User workspace",
                    "displayLabel": "What is your workspace Azure Defender Plan Settings?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "On",
                            "text": "On"
                        },
                        {
                            "value": "Off",
                            "text": "Off"
                        }
                    ],
                    "required": false
                },{
                    "id": "tier_type",
                    "order": 7,
                    "controlType": "dropdown",
                    "displayLabel": "What is your Data Collection tier?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "None",
                            "text": "None"
                        },
                        {
                            "value": "Minimal",
                            "text": "Minimal"
                        },
						{
                            "value": "Common",
                            "text": "Common"
                        },
						{
                            "value": "All",
                            "text": "All"
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
