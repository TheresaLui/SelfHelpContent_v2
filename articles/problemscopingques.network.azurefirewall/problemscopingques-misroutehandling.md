<properties
	articleId="problemscopingques-misroutehandling"
	pageTitle="Azure Firewall Generic"
	description="Azure Firewall Generic"
	authors="spacest"
	ms.author="mariliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32628805,32608919,32608920,32628807,32628806,32608924,32608918,32608921,32608922,32608917"
	productPesIds="16556"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# VM Performance
---
{
	"resourceRequired": true,
	"title": "Slow virtual machine",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "slow_vm_determination",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "How did you determine that your virtual machine was slow?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "It's slower that it typically is",
					"text": "It's slower that it typically is"
				}, {
					"value": "Another virtual machine in the subscription is faster",
					"text": "Another virtual machine in the subscription is faster"
				}, {
					"value": "Benchmarking tests not meeting minimum Azure specifications",
					"text": "Benchmarking tests not meeting minimum Azure specifications"
				}, {
					"value": "It's faster in a non-Azure environment",
					"text": "It's faster in a non-Azure environment"
				}
			],
			"required": false
		}, {
			"id": "problem_start_time",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "applications_on_vm",
			"order": 3,
			"controlType": "multiselectdropdown",
			"displayLabel": "Select the applications running on your virtual machine",
			"dropdownOptions": [{
					"value": "CRM Dynamics",
					"text": "CRM Dynamics"
				}, {
					"value": "IIS / Web Front end",
					"text": "IIS / Web Front end"
				}, {
					"value": "MySQL",
					"text": "MySQL"
				}, {
					"value": "Oracle",
					"text": "Oracle"
				}, {
					"value": "Remote Desktop Services",
					"text": "Remote Desktop Services"
				}, {
					"value": "SAP Hanna",
					"text": "SAP Hanna"
				}, {
					"value": "SharePoint",
					"text": "SharePoint"
				}, {
					"value": "SQL",
					"text": "SQL"
				}, {
					"value": "Other (describe below)",
					"text": "Other"
				}
			],
			"required": false
		}, {
			"id": "problem_description",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Issue description."
				}, {
					"text": "Name of the virtual machine(s) in the same subscription that you think is faster than the slow virtual machine."
				}
			]
		}, {
			"id": "learn_more_text",
			"order": 6,
			"controlType": "infoblock",
			"content": "<a href='https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-sizes?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json'>Learn more</a> about virtual machine specifications for IOPS (input/output operations per second) and our recommended benchmarking tools"
		}
	]
}
---
