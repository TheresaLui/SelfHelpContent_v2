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
			"id": "learn_more_text",
			"order": 1,
			"controlType": "infoblock",
			"content": "<b>Please review the resources listed below prior to opening a support case</b>  <ul><li><a href='https://aka.ms/intunetroubleshooting1'>Click here</a> to troubleshoot with the Intune Troubleshooting Blade</li>  <li><a href='https://docs.microsoft.com/intune/ios-enroll'>Click here</a> to review our iOS enrollment documentation</li>  <li><a href='https://docs.microsoft.com/intune/macos-enroll'>Click here</a> to review our mac OS enrollment documentation</li>  <li><a href='https://aka.ms/intuneforums'>Review our Intune TechNet forums</a> to find answers and solutions to common issues</li>  <li><a href='https://portal.office.com/AdminPortal/Home#/MessageCenter'>Click here</a> to see the current status of the service</li></ul>"
		},  {
			"id": "What service are you having the issue with?",
			"order": 4,
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
			"order": 5,
			"controlType": "dropdown",
			"displayLabel": "What problem are you having?",
			"watermarkText": "Choose a problem",
			"dropdownOptions": [{
					"value": "Cannot enroll Apple device(s)",
					"text": "Cannot enroll Apple device(s)"
				}, {
					"value": "Cannot setup Apple MDM Push Certificate",
					"text": "Cannot setup Apple MDM Push Certificate"
				}, {
					"value": "Cannot configure Apple Configurator Profile",
					"text": "Cannot configure Apple Configurator Profile"
				}, {
					"value": "Cannot login to Company Portal application to enroll a device",
					"text": "Cannot login to Company Portal application to enroll a device"
				}, {
					"value": "Cannot setup Apple Device Enrollment (DEP) Program or Apple School Manager (ASM) token",
					"text": "Cannot setup Apple Device Enrollment (DEP) Program or Apple School Manager (ASM) token"
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
			"id": "problem_who_is_impacted",
			"order": 6,
			"controlType": "textbox",
			"displayLabel": "Who is impacted?",
			"watermarkText": "Enter UPN, e-mail addresses, serial or IMEI numbers here, if multiple separate by semi-colon",
			"useAsAdditionalDetails": false,
			"required": true,
			"hints": [{
					"text": "For user based enrollment provide UPN or e-mail addresses.  For userless enrollment provide serial or IMEI numbers"
				}
			]
		}, {
			"id": "What devices types are impacted?",
			"order": 7,
			"controlType": "multiselectdropdown",
			"displayLabel": "Select device types that are impacted",
			"dropdownOptions": [{
					"value": "iPad",
					"text": "iPad"
				}, {
					"value": "iPhone",
					"text": "iPhone"
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
			"id": "How are these devices managed?",
			"order": 8,
			"controlType": "multiselectdropdown",
			"displayLabel": "How are these devices managed?",
			"dropdownOptions": [{
					"value": "Bring-your-own-device (BYOD)",
					"text": "Bring-your-own-device (BYOD)"
				}, {
					"value": "Corporate-owned",
					"text": "Corporate-owned"
				}, {
					"value": "Device Enrollment Program (DEP)",
					"text": "Device Enrollment Program (DEP)"
				}, {
					"value": "Apple School Manager (ASM)",
					"text": "Apple School Manager (ASM)"
				}, {
					"value": "Apple Configurator",
					"text": "Apple Configurator"
				}
			],
			"required": false
		}, {
			"id": "How many users are impacted?",
			"order": 9,
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
			"id": "problem_start_date",
			"order": 10,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem start?",
			"required": false
		}, {
			"id": "problem_details",
			"order": 11,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide these details:",
			"watermarkText": "Enter details here",
			"required": true,
			"useAsAdditionalDetails": false,
			"hints": [{
					"text": "Issue description that includes device names, error message(s) and scenario(s) that are failing."
				}, {
					"text": "Using file upload on the left, attach a screenshot of the error message(s) or any logs/documentation gathered."
				}
			]
		}
]}
---
