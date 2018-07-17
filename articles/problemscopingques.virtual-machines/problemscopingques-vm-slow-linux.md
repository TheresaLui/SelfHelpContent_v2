<properties
	pageTitle="Slow virtual machine - Linux"
	description="Slow virtual machine - Linux"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32411877"
	productPesIds="15571,15797,16454"
	cloudEnvironments="Public"
	schemaVersion="1"
/>
# VM Performance
---
{
	"resourceRequired": true,
	"title": "Slow virtual machine - Linux",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "problem_start_date",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "Start time of most recent occurrence",
			"required": true
		}, {
			"id": "disk_path",
			"order": 2,
			"controlTye": "textbox",
			"displayLabel": "If the performance issue is specific to a disk, provide disk path",
			"watermarkText": "StorageAccount/Container/DiskName.vhd",
			"required": false
		}, {
			"id": "additional_details",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide these details",
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
			"order": 5,
			"controlType": "infoblock",
			"content": "<a href='https://docs.microsoft.com/azure/virtual-machines/linux/sizes'>Learn more</a> about virtual machine specifications for IOPS (input/output operations per second) and our recommended benchmarking tools"
		}
	]
}
---
