<properties
	pageTitle="Azure Information Protection - Creating and configuring Labels and Policies - Creating Labels"
	description="Azure Information Protection - Creating and configuring Labels and Policies - Creating Labels"
	authors="orbarak-ms"
	ms.author="orbarak"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32727941"
    productPesIds="14997"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_configpolicy_creatinglabel"
	schemaVersion="1"
	ownershipId="AzureIdentity_InformationProtection"
/>
# Can't apply this label
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Creating and configuring Labels and Policies",
				"subscriptionRequired": false,
                "fileAttachmentHint": "Export AIP logs Using Protect/Sensitivity button - Help and Feedback - Export Logs",
                "formElements": [
                {
                    "id": "client_type",
                    "order": 2,
                    "controlType": "dropdown",
                    "displayLabel": "Which AIP client are you using?",
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
                    "id": "office_type",
                    "order": 6,
                    "controlType": "dropdown",
                    "displayLabel": "Which Office version are you using?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Office 20XX Standard (Not supported for Protection)",
                            "text": "Office 20XX Standard (Not supported for Protection)"
                        },
                        {
                            "value": "Office 20XX ProPlus (Microsoft Apps for Enterprise)",
                            "text": "Office 20XX ProPlus (Microsoft Apps for Enterprise)"
                        },
                        {
                            "value": "Office 365 Click-To-Run",
                            "text": "Office 365 Click-To-Run"
                        },	                    {
							"value": "dont_know_answer",
							"text": "None of the above"
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
