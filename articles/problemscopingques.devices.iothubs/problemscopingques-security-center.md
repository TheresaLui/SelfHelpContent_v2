<properties
	pageTitle="Issues with IoT Hub azure security center"
	description="Issues with azure security center for IoT Hub scoping questions"
	authors="camanle"
	ms.author="camanle"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32636058"
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-security-center"
	ownershipId="AzureIot_IotHub"
/>

# IoT Hub azure security center issues

---

{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
  "title": "IoT Hub azure security center issues",
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
      "id": "security",
      "order": 2,
      "controlType": "dropdown",
      "displayLabel": "Which area of ASC are you having issues with?",
      "dropdownOptions": [{
					"value": "Recommendations",
					"text": "Recommendations"
				}, {
					"value": "Alerts",
					"text": "Alerts"
				}, {
					"value": "Security agents and SDK",
					"text": "Security agents and SDK"
				}, {
					"value": "Configuration",
					"text": "Configuration"
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