<properties
	pageTitle="Azure Information Client - Manual protection"
	description="Azure Information Client - Manual protection"
	authors="orbarak-ms"
	ms.author="orbarak"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32584355"
    productPesIds="14997"
    cloudEnvironments="Public, Fairfax"
    articleId="scoping_manual_protection"
	schemaVersion="1"
/>
# Can't apply this label
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Manual Protection",
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
                "id": "version_number",
                "order": 3,
				"visibility": "client_type == Azure Information Protection client (classic)",
                "controlType": "textbox",
                "displayLabel": "What version are you using? For details, use the link in the help balloon",
				"infoBalloonText": "Verify that you use a <a href='https://docs.microsoft.com/azure/information-protection/rms-client/client-version-release-history'>supported version</a>",
                "required": true
                },{
                "id": "version_number_ul",
                "order": 4,
				"visibility": "client_type == Azure Information Protection Unified Labeling Client",
                "controlType": "textbox",
                "displayLabel": "What version are you using? For details, use the link in the help balloon",
				"infoBalloonText": "Verify that you use a <a href='https://docs.microsoft.com/azure/information-protection/rms-client/unifiedlabelingclient-version-release-history'>supported version</a>",
                "required": true
                },{
                    "id": "checkrightclick",
                    "order": 6,
                    "controlType": "dropdown",
                    "displayLabel": "Were you able to replicate this issue using Right Click - Classify and Protect",
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
