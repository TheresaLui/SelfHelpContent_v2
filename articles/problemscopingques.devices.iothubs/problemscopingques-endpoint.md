<properties
	pageTitle="Issues with IoT Hub endpoints"
	description="Issues with endpoints for IoT Hub scoping questions"
	authors="camanle"
	ms.author="camanle"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32783521"
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-endpoint"
	ownershipId="AzureIot_IotHub"
/>

# IoT Hub endpoint issues

---

{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
  "title": "IoT Hub endpoint issues",
  "fileAttachmentHint": "Upload screenshots of errors if available",
  "formElements": [
    {
      "id": "problem_start_time",
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem start?",
      "required": true
    },
    {
      "id": "new_endpoint",
      "order": 2,
      "controlType": "dropdown",
      "displayLabel": "Is this a new endpoint?",
      "dropdownOptions": [{
					"value": "Yes",
					"text": "Yes"
				}, {
					"value": "No",
					"text": "No"
				}, {
					"value": "dont_know_answer",
					"text": "Don't Know"
				}
			],
      "required": false
    },
    {
      "id": "working_endpoint",
      "order": 4,
      "controlType": "dropdown",
      "displayLabel": "Has data been successfully flowed to this endpoint before?",
      "dropdownOptions": [{
					"value": "Yes",
					"text": "Yes"
				}, {
					"value": "No",
					"text": "No"
				}, {
					"value": "dont_know_answer",
					"text": "Don't Know"
				}
			],
      "required": false
    },
    {
      "id": "problem_description",
      "order": 5,
      "controlType": "multilinetextbox",
      "displayLabel": "Description",
      "watermarkText": "Provide additional information about your issue",
      "required": true,
      "useAsAdditionalDetails": true,
      "hints": [
        {
          "text": "Description of the issue and repro steps"
        },
        {
          "text": "Error logs with timestamp (indicate timezone or UTC)"
        }
      ]
    }
  ]

}
---