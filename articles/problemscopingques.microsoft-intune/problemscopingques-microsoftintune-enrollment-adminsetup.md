<properties
	pageTitle="Enrollment Options"
	description="Enrollment Options"
	authors="mackie1604"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32530429"
	productPesIds="15584"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Enrollment Options
---
{
	"resourceRequired": false,
	"title": "Enrollment Options",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "learn_more_text",
			"order": 1,
			"controlType": "infoblock",
			"content": "<b>Please review the resources listed below prior to opening a support case</b>  <ul><li><a href='https://aka.ms/intunetroubleshooting1'>Click here</a> to troubleshoot with the Intune Troubleshooting Blade</li>  <li><a href='https://docs.microsoft.com/intune/enrollment-options'>Click here</a> to review our enrollment options documentation</li>  <li><a href='https://aka.ms/intuneforums'>Review our Intune TechNet forums</a> to find answers and solutions to common issues</li>  <li><a href='https://portal.office.com/AdminPortal/Home#/MessageCenter'>Click here</a> to see the current status of the service</li</ul>"
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
			"id": "EnrollmentOptions_problem_determination",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "What problem are you having?",
			"watermarkText": "Choose a problem",
			"dropdownOptions": [{
					"value": "Cannot configure/deploy Terms and Conditions",
					"text": "Cannot configure/deploy Terms and Conditions"
				}, {
					"value": "Cannot setup enrollment restrictions",
					"text": "Cannot setup enrollment restrictions"
				}, {
					"value": "Cannot setup Multi-Factor Authentication for enrollment",
					"text": "Cannot setup Multi-Factor Authentication for enrollment"
				}, {
					"value": "Cannot setup Device Enrollment Manager(s)",
					"text": "Cannot setup Device Enrollment Manager(s)"
				}, {
					"value": "Cannot setup Device Categories",
					"text": "Cannot setup Device Categories"
				}, {
					"value": "Cannot setup Corporate Device Identifiers",
					"text": "Cannot setup Corporate Device Identifiers"
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
			"id": "What platforms are impacted?",
			"order": 5,
			"controlType": "multiselectdropdown",
			"displayLabel": "What platforms are impacted?",
			"dropdownOptions": [{
					"value": "Apple",
					"text": "Apple"
				}, {
					"value": "Android",
					"text": "Android"
				}, {
					"value": "Windows",
					"text": "Windows"
				}, {
					"value": "Other",
					"text": "Other"
				}
			],
			"required": false
		}, {
			"id": "How many users are impacted?",
			"order": 6,
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
			"order": 7,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem start?",
			"required": false
		}, {
			"id": "problem_details",
			"order": 8,
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
