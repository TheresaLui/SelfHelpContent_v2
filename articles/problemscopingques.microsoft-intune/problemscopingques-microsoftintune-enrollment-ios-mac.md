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
					"value": "Cannot enroll a BYOD iOS device",
					"text": "Cannot enroll a BYOD iOS device"
				}, {
					"value": "Cannot enroll a DEP or Supervised iOS device",
					"text": "Cannot enroll a DEP or Supervised iOS device"
				}, {
					"value": "Cannot enroll a Mac device",
					"text": "Cannot enroll a Mac device"
				}, {
					"value": "Cannot setup my Apple MDM Push Certificate",
					"text": "Cannot setup my Apple MDM Push Certificate"
				}, {
					"value": "Cannot setup my Apple DEP Token",
					"text": "Cannot setup my Apple DEP Token"
				}, {
					"value": "Cannot login to Company Portal application to enroll a device",
					"text": "Cannot login to Company Portal application to enroll a device"
				}, {
					"value": "Cannot enroll a Apple Configurator device",
					"text": "Cannot enroll a Apple Configurator device"
				}, {
					"value": "Cannot configure an Apple Configurator Profile",
					"text": "Cannot configure an Apple Configurator Profile"
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
			"watermarkText": "Enter UPN or E-Mail addresses here, if multiple seperate by semi-colon",
			"useAsAdditionalDetails": false,
			"required": true,
			"hints": [{
					"text": "What users are impacted?  Please provide UPNs of the impacted users."
				}
			]
		}, {
			"id": "What devices types are impacted?",
			"order": 4,
			"controlType": "multiselectdropdown",
			"displayLabel": "Select the device types that are impacted",
			"dropdownOptions": [{
					"value": "iPhone",
					"text": "iPhone"
				}, {
					"value": "iPad",
					"text": "iPad"
				}, {
					"value": "iPod",
					"text": "iPod"
				}, {
					"value": "Mac",
					"text": "Mac"
				}
			],
			"required": false
		}, {
			"id": "How many users are impacted?",
			"order": 5,
			"controlType": "dropdown",
			"displayLabel": "Select how many users are impacted",
			"dropdownOptions": [{
					"value": "Single user",
					"text": "Single user"
				}, {
					"value": "A few users",
					"text": "A few users"
				}, {
					"value": "Most of my users",
					"text": "Most of my users"
				}, {
					"value": "All my users",
					"text": "All my users"
				}
			],
			"required": false
		}, {
			"id": "problem_details",
			"order": 6,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide these details:",
			"watermarkText": "Enter details here",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Issue description that includes device names, error message(s) and scenario(s) that are failing."
				}, {
					"text": "Using file upload on the left, attach a screenshot of the error message or any logs/documentation you've gathered."
				}
			]
		}
]}
---
