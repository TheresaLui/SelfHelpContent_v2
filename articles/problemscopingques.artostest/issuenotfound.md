<properties
	pageTitle="Azure RTOS Issues"
	description="Azure RTOS Scoping Questions to capture more information"
	authors="michamay"
	ms.author="micmay"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32725736"
	productPesIds="16920"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="65a4348a-2bab-4ab0-b5dc-4330ff026530"
	ownershipId="Azure_RTOS"
/>
# Problem Description
---
{
	"$schema": "SelfHelpContent",
	"subscriptionRequired": false,
	"resourceRequired": false,
	"title": "What version are you using",
	"fileAttachmentHint": "",
	"formElements": [{
		"id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "infoBalloonText": "Enter the approximate time you started to see the error.",
            "required": true
       }, {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem stop? (If ongoing, leave this field blank)",
            "infoBalloonText": "Enter when the error stopped, or leave blank if the issue is ongoing.",
            "required": false
        }, {
		"id": "I'm experienceing errors when setting up Azure RTOS",
		"order": 3,
		"controlType": "multiselectdropdown",
		"infoBalloonText": "string",
		"displayLabel": "In which product(s) are you experiencing the problem",
		"watermarkText": "Choose an option",
		"dropdownOptions": [{
			"value": "Azure RTOS ThreadX",
			"text": "Azure RTOS ThreadX"
		}, {
			"value": "Azure RTOS NetX",
			"text": "Azure RTOS NetX"
		}, {
			"value": "Azure RTOS NetX Duo",
			"text": "Azure RTOS NetX Duo"
		}, {
			"value": "Azure RTOS FileX",
			"text": "Azure RTOS FileX"
		}, {
			"value": "Azure RTOS USBX",
			"text": "Azure RTOS USBX"
		}, {
			"value": "Azure RTOS GUIX",
			"text": "Azure RTOS GUIX"
		}, {
			"value": "Azure RTOS GUIX Studio",
			"text": "Azure RTOS GUIX Studio"
		}, {
			"value": "Azure RTOS TraceX",
			"text": "Azure RTOS TraceX"
		}],
		"required": false
	}, {
		"id": "problem_description",
		"order": 4,
		"controlType": "multilinetextbox",
		"displayLabel": "Please provide a description of the problem including",
		"watermarkText": "provide as much of the above information here as you can",
		"required": true,
		"useAsAdditionalDetails": true,
		"hints": [{
			"text": "A list of the events that manifested the problem."
		}, {
			"text": "Any recent code changes or updates that might have triggered the issue."
		}, {
			"text": "The contents of the 'build_option' variable."
		}, {
			"text": "An instruction trace, if available."
		}, {
			"text": "A sample program that exhibits the problem, if possible."
		}]
	}, {
		"id": "User Guides",
		"order": 5,
		"controlType": "infoblock",
		"content": "<a href='https://docs.microsoft.com/azure/rtos/'>please refer to the User Guide</a> for more information"
	}]
}
---
