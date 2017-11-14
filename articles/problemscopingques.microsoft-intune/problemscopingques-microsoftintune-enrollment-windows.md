<properties
	pageTitle="Intune Enrollment Windows"
	description="Intune Enrollment Windows"
	authors="mackie1604"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32530438"
	productPesIds="15584"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Intune Enrollment Windows
---
{
	"resourceRequired": false,
	"title": "Intune Enrollment Windows",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "learn_more_text",
			"order": 1,
			"controlType": "infoblock",
			"content": "<ul><li><a href='https://aka.ms/intunetroubleshooting1'>Click here</a> to troubleshoot with the Intune Troubleshooting Blade</li>  <li><a href='https://docs.microsoft.com/intune/windows-enroll'>Click here</a> to review our Windows enrollment documentation</li>  <li><a href='https://aka.ms/intuneforums'>Review our Intune TechNet forums</a> to find answers and solutions to common issues</li>  <li><a href='https://portal.office.com/AdminPortal/Home#/MessageCenter'>Click here</a> to check the status of the service and review other service alerts</li></ul>"
		},  {
			"id": "What service are you having the issue with?",
			"order": 2,
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
			"id": "Windows_problem_determination",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "What problem are you having?",
			"watermarkText": "Choose a problem",
			"dropdownOptions": [{
					"value": "Cannot enroll Windows 10 Modern device(s)",
					"text": "Cannot enroll Windows 10 Modern device(s)"
				}, {
					"value": "Cannot enroll Windows 10 Mobile device(s)",
					"text": "Cannot enroll Windows 10 Mobile device(s)"
				}, {
					"value": "Cannot setup Windows 10 automatic enrollment",
					"text": "Cannot setup Windows 10 automatic enrollment"
				}, {
					"value": "Cannot setup bulk enrollment for Windows 10",
					"text": "Cannot setup bulk enrollment for Windows 10"
				}, {
					"value": "Cannot login to Company Portal application to enroll a device",
					"text": "Cannot login to Company Portal application to enroll a device"
				}, {
					"value": "Cannot setup Windows AutoPilot Deployment Program",
					"text": "Cannot setup Windows AutoPilot Deployment Program"
				}, {
					"value": "Cannot setup Windows Hello for Business",
					"text": "Cannot setup Windows Hello for Business"
				}, {
					"value": "Cannot validate CNAME",
					"text": "Cannot validate CNAME"
				}, {
					"value": "Cannot configure Enrollment Status Screen",
					"text": "Cannot configure Enrollment Status Screen"
				}, {
					"value": "Other",
					"text": "Other"
				}
			],
			"required": true
		}, {
			"id": "problem_who_is_impacted",
			"order": 4,
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
			"id": "What Operating System(s) are impacted?",
			"order": 5,
			"controlType": "multiselectdropdown",
			"displayLabel": "What Operating System(s) are impacted?",
			"dropdownOptions": [{
					"value": "Windows 10 1511 or earlier",
					"text": "Windows 10 1511 or earlier"
				}, {
					"value": "Windows 10 1607",
					"text": "Windows 10 1607"
				}, {
					"value": "Windows 10 1703",
					"text": "Windows 10 1703"
				}, {
					"value": "Windows 10 1709 or greater",
					"text": "Windows 10 1709 or greater"
				}, {
					"value": "Windows 8.1",
					"text": "Windows 8.1"
				}, {
					"value": "Other",
					"text": "Other"
				}
			],
			"required": false
		}, {
			"id": "How are these devices managed?",
			"order": 6,
			"controlType": "multiselectdropdown",
			"displayLabel": "How are these devices managed?",
			"dropdownOptions": [{
					"value": "Bring your own device",
					"text": "Bring your own device"
				}, {
					"value": "EDU",
					"text": "EDU"
				}, {
					"value": "Co-Management",
					"text": "Co-Management"
				}, {
					"value": "AutoPilot",
					"text": "AutoPilot"
				}
			],
			"required": false
		}, {
			"id": "How many users are impacted?",
			"order": 7,
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
			"order": 8,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem start?",
			"required": false
		}, {
			"id": "problem_details",
			"order": 9,
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
