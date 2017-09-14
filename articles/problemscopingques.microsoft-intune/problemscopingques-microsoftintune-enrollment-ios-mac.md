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
			"id": "What service are you having the issue with?",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Select the service impacted",
			"watermarkText": "Choose your service",
			"dropdownOptions": [{
					"value": "Intune Standalone",
					"text": "Intune Standalone"
				}, {
					"value": "Intune Hybrid",
					"text": "Intune Hybrid"
				}, {
					"value": "Intune for Education",
					"text": "Intune for Education"
				}, {
					"value": "Intune Insiders",
					"text": "Intune Insiders"
				}, {
					"value": "Mobile Device Management for Office 365",
					"text": "Mobile Device Management for Office 365"
				}
			],
			"required": true
		},  {
			"id": "iOSMAC_problem_determination",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "What problem are you having?",
			"watermarkText": "Choose a problem",
			"dropdownOptions": [{
					"value": "Cannot enroll Apple device(s)",
					"text": "Cannot enroll Apple device(s)"
				}, {
					"value": "Cannot setup my Apple MDM Push Certificate",
					"text": "Cannot setup my Apple MDM Push Certificate"
				}, {
					"value": "Cannot configure an Apple Configurator Profile",
					"text": "Cannot configure an Apple Configurator Profile"
				}, {
					"value": "Cannot login to Company Portal application to enroll a device",
					"text": "Cannot login to Company Portal application to enroll a device"
				}, {
					"value": "Cannot setup my Apple DEP or Apple School Manager token",
					"text": "Cannot setup my Apple DEP or Apple School Manager token"
				}, {
					"value": "Cannot configure Enrollment Program Profile",
					"text": "Cannot configure Enrollment Program Profile"
				}, {
					"value": "Other",
					"text": "Other"
				}
			],
			"required": true
		}, {
			"id": "iOSMAC_problem_determination_Other",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "If "other" please describe the problem you're having.",
			"watermarkText": "Describe "other" problem here",
			"required": false
		}, {
			"id": "problem_start_date",
			"order": 4,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": false
		}, {
			"id": "problem_who_is_impacted",
			"order": 5,
			"controlType": "textbox",
			"displayLabel": "Who is impacted?",
			"watermarkText": "Enter UPN or E-Mail addresses here, if multiple seperate by semi-colon",
			"useAsAdditionalDetails": false,
			"required": false,
			"hints": [{
					"text": "What users are impacted?  Please provide UPNs of the impacted users."
				}
			]
		}, {
			"id": "What devices types are impacted?",
			"order": 6,
			"controlType": "multiselectdropdown",
			"displayLabel": "Select device types that are impacted",
			"dropdownOptions": [{
					"value": "iPad",
					"text": "iPad"
				}, {
					"value": "iPhone",
					"text": "iPhone"
				}, {
					"value": "Mac",
					"text": "Mac"
				}
			],
			"required": false
		}, {
			"id": "How are these devices managed?",
			"order": 7,
			"controlType": "multiselectdropdown",
			"displayLabel": "How are these devices managed?",
			"dropdownOptions": [{
					"value": "BYOD",
					"text": "BYOD"
				}, {
					"value": "DEP",
					"text": "DEP"
				}, {
					"value": "Configurator",
					"text": "Configurator"
				}
			],
			"required": false
		}, {
			"id": "How many users are impacted?",
			"order": 8,
			"controlType": "dropdown",
			"displayLabel": "Select how many users are impacted",
			"watermarkText": "Users impacted",
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
			"order": 9,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide these details:",
			"watermarkText": "Enter details here",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Issue description that includes device names, error message(s) and scenario(s) that are failing."
				}, {
					"text": "Using file upload on the left, attach a screenshot of the error message(s) or any logs/documentation gathered."
				}
			]
		}
]}
---
