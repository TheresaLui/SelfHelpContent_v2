<properties
	pageTitle="Azure Information Client - Installing, Onboarding, or Decommissioning - RMS connector setup and configuration"
	description="Azure Information Client - Installing, Onboarding, or Decommissioning - RMS connector setup and configuration"
	authors="orbarak-ms"
	ms.author="orbarak"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32727966"
    productPesIds="14997"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_installation_issues_rmsconnector"
	schemaVersion="1"
	ownershipId="AzureIdentity_InformationProtection"
/>
# Can't apply this label
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Installation Issues",
				"subscriptionRequired": false,
                "fileAttachmentHint": "Navigate to %temp% and include MSI installer logs",
                "formElements": [
                {
                    "id": "client_type",
                    "order": 2,
                    "controlType": "dropdown",
                    "displayLabel": "Did the RMS Connector install successfully?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "install_Yes",
                            "text": "Yes"
                        },
                        {
                            "value": "install_No",
                            "text": "No"
                        },
	                    {
							"value": "dont_know_answer",
							"text": "I don't know"
						}
                    ],
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
