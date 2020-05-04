<properties
	pageTitle="Azure RTOS Issues"
	description="Azure RTOS Scoping Questions to capture more information"
	authors="michamay"
	ms.author="micmay"
	selfHelpType="problemScopingQuestions"	supportTopicIds="32725731,32725732,32725744,32725739,32725740,32725741,32725742,32725743,32725738,32725745,32725746,32725736,32725725"
	productPesIds="16920"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="65a4348a-2bab-4ab0-b5dc-4330ff026530"
	ownershipId="Azure_RTOS"
/>
# Problem Desscription
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
		"order": 2,
		"controlType": "multiselectdropdown",
		"infoBalloonText": "string",
		"displayLabel": "What product(s) are you using?",
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
			"text": "Azure RTOS GUIX Studi"
		}, {
			"value": "Azure RTOS TraceX",
			"text": "Azure RTOS TraceX"
		}],
		"required": false
	}, {
		"id": "problem_description",
		"order": 3,
		"controlType": "multilinetextbox",
		"displayLabel": "Details",
		"watermarkText": "Please provide a description of the problem including",
		"required": true,
		"useAsAdditionalDetails": true,
		"hints": [{
			"text": "How reproducible is the problem?"
		}, {
			"text": "List the sequence of events that manifested the problem."
		}, {
			"text": "Were there any recent code changes or updates that might have triggered the issue?"
		}, {
			"text": "What are the contents of the build_options variable?"
		}, {
			"text": "Do you have an instruction trace?"
		}, {
			"text": "Do you have a sample program that exhibits the problem?"
		}]
	}, {
		"id": "User Guides",
		"order": 4,
		"controlType": "infoblock",
		"content": "<a href='https://docs.microsoft.com/azure/rtos/'>please refer to the User Guide</a> for more information"
	}]
}
---
