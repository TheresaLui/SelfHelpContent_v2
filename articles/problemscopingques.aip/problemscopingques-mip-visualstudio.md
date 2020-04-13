<properties
	pageTitle="MIP SDK - VSInteg"
	description="MIP SDK - VSInteg"
	authors="orbarak-ms"
	ms.author="orbarak"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32584382"
    productPesIds="14997"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
    articleId="scoping_mip_vsinteg"
	schemaVersion="1"
	ownershipId="AzureIdentity_InformationProtection"
/>
# Can't apply this label
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "SDK Visual Studio Integration",
				"subscriptionRequired": false,
                "fileAttachmentHint": "Provide logs for MIP SDK: from the mip_data directory and for RMS SDK from %SystemDrive%\\\\ProgramData\\\\MSIPC\\\\SID",
                "formElements": [
                {
                    "id": "client_type",
                    "order": 2,
                    "controlType": "dropdown",
                    "displayLabel": "Which SDK are you using?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "RMS SDK",
                            "text": "RMS SDK"
                        },
                        {
                            "value": "MIP SDK",
                            "text": "MIP SDK"
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
                "controlType": "textbox",
                "displayLabel": "What version of the SDK are you using? Did you upgrade to the latest version?",
                "required": true
                },{
                "id": "sample_code",
                "order": 4,
                "controlType": "textbox",
                "displayLabel": "Did you use a sample code? Did it work?"
                },{
                    "id": "sccmigrate",
                    "order": 5,
                    "controlType": "dropdown",
                    "displayLabel": "Are you trying to work against ADRMS or AzureRMS?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "ADRMS",
                            "text": "ADRMS"
                        },
                        {
                            "value": "AzureRMS",
                            "text": "AzureRMS"
                        }
                    ],
                    "required": false
                },{
                    "id": "problem_description",
                    "order": 1,
                    "controlType": "multilinetextbox",
                    "displayLabel": "Description - What were you trying to do?",
                    "useAsAdditionalDetails": true,
                    "required": true
                    },{
                    "id": "problem_start_time",
                    "order": 7,
                    "controlType": "datetimepicker",
                    "displayLabel": "When did the problem start?",
                    "required": true
                  }
                  ]
}
---
