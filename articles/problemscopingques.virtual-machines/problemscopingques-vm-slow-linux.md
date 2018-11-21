<properties
	pageTitle="Slow virtual machine - Linux"
	description="Slow virtual machine - Linux"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32628264,32628261,32628277,32628254,32628275,32628268,32628281,32628270"
	productPesIds="15571,15797,16454"
	cloudEnvironments="Public"
	schemaVersion="1"
	articleId="8674f1c2-3103-413c-8c07-49432abc6f27"
/>
# VM Performance
---
{
    "resourceRequired": true,
    "title": "Slow virtual machine - Linux",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Start time of most recent occurrence",
            "required": true
        },
        {
            "id": "disk_path",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "If the performance issue is specific to a disk, provide disk path",
            "watermarkText": "StorageAccount/Container/DiskName.vhd",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide these details",
            "required": false,
            "useAsAdditionalDetails": true
        },
        {
            "id": "learn_more_text",
            "order": 4,
            "controlType": "infoblock",
            "content": "<a href='https://docs.microsoft.com/azure/virtual-machines/linux/sizes'>Learn more</a> about virtual machine specifications for IOPS (input/output operations per second) and our recommended benchmarking tools"
        }
    ]
}
---
