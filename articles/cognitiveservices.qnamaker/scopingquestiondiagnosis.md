<properties
	pageTitle="Scoping question for permission to access diagnostic data"
	description="Scoping question for permission to access diagnostic data"
	service="cognitiveService-qnamaker"
	resource="qnamaker"
	authors="NehaRajput"
	ms.author="nerajput"
	displayOrder="1"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32689790"
	productPesIds="16919"
	schemaVersion="1"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="5b9b1a32-b82e-740c-f2d9-d84b0a070d76"
	ownershipId="AzureCogSvc_CognitiveServices"
/>

# Diagnosis
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": false,
  "formElements":
  [
  {
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "Incident time",
			"required": true
		},
    {
      "id": "consent_radio_button",
      "order": 2,
      "controlType": "radioButtonGroup",
      "displayLabel": "Consent:",
      "radioButtonOptions":
      [{
            "value": "AllowCustomerDataAccess",
            "text": "Allow Azure support to gather diagnostic information from your Azure resource."
        },
        {
            "value": "DonotAllowCustomerDataAccess",
            "text": "Do not share diagnostic information."
        }
      ],
    "required": true
    },
    {
			"id": "problem_description",
			"order": 3,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your incident including any error messages you are seeing.",
			"required": true,
			"useAsAdditionalDetails": true
		}
  ]
}

---
