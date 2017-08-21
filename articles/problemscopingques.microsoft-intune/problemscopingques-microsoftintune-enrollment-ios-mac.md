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
	"resourceRequired": true,
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
			"required": false
		}, {
			"id": "problem_start_date",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "problem_details",
			"order": 3,
			"controlType": "multilinetextbox",
			"displayLabel": "Please describe the problem in detail",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Provide device type, OS version and any error messages observed."
				}, {
					"text": "Attach screenshots if possible of the error message using the file uploader."
				}
			]
		}
]}
---
