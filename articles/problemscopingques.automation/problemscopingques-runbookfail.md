<properties
	articleId="problemscopingques-runbookfail.md"
	pageTitle="Azure Automation - Runbook Execution"
	description="Azure Automation - Runbook Execution"
	authors="zjalexander"
	ms.author="zachal"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32599860,32599923,32599906,32599907,32599908,32599909,32615224,32628014,32628013"
	productPesIds="15607"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Runbook Execution
---
{
	"resourceRequired": true,
	"title": "Runbook failure",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "runbook selection",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Select the runbook that has the problem",
			"watermarkText": "Choose a runbook",
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
			"required": true
		}, {
			"id": "problem_start_date",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": false
		}, {
			"id": "previously successful",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Has this runbook successfully run in Azure Automation before?",
			"dropdownOptions": [{
					"value": "Yes",
					"text": "Yes, this runbook has successfully run in Azure Automation before"
				}, {
					"value": "No",
					"text": "No, this runbook has never successfully run in Azure Automation"
				}
			],
			"required": false
		}, {
			"id": "problem_description",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue",
			"required": false,
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
