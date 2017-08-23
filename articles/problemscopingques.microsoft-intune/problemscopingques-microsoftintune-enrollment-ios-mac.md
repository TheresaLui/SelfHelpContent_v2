<properties
	pageTitle="Set up iOS and Mac device management"
	description="Set up iOS and Mac device management"
	authors="mackie1604"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32530435"
	productPesIds="15584"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Set up iOS and Mac device management
---
{
	"resourceRequired": false,
	"title": "Set up iOS and Mac device management",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "iOSMAC_problem_determination",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "What problem are you having?",
			"watermarkText": "Choose a problem",
			"dropdownOptions": [{
					"value": "Cannot enroll a BYOD iOS Device",
					"text": "Cannot enroll a BYOD iOS Device"
				}, {
					"value": "Cannot enroll a DEP or Supervised iOS device",
					"text": "Cannot enroll a DEP or Supervised iOS device"
				}, {
					"value": "Cannot enroll a Mac Device",
					"text": "Cannot enroll a Mac Device"
				}, {
					"value": "Cannot setup my Apple MDM Push Certificate",
					"text": "Cannot setup my Apple MDM Push Certificate"
				}, {
					"value": "Cannot setup my Apple DEP Token",
					"text": "Cannot setup my Apple DEP Token"
				}, {
					"value": "Cannot login to Company Portal application to enroll a device",
					"text": "Cannot login to Company Portal application to enroll a device"
				}
			],
			"required": true
		}, {
			"id": "problem_start_date",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "problem_who_is_impacted",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "Who is impacted?",
			"watermarkText": "Enter UPN or E-Mail address here",
			"useAsAdditionalDetails": false,
			"required": true,
			"hints": [{
					"text": "What users are impacted?  Please provide UPNs of the impacted users."
				}
			]
		}, {
			"id": "problem_details",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide these details:",
			"watermarkText": "Enter details here",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Issue description that includes device names, error message and scenario that is failing."
				}, {
					"text": "Using file upload on the left, attach a screenshot of the error message or any logs/documentation you've gathered."
				}
			]
		}
]}
---
