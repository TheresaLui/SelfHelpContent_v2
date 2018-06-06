<properties
	pageTitle="Deploy a New VM"
	description="Deploy a New VM"
	authors="scottAzure"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32411844"
	productPesIds="14749"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Deploy a New VM
---
{
	"resourceRequired": false,
	"title": "Deploy a New VM",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "deploymentfailure_determination",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Do you have a deployment error for this issue?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "true",
					"text": "Yes"
				}, {
					"value": "false",
					"text": "No"
				}, {
					"value": "unknown",
					"text": "I don't know"
				}
			],
			"required": false
		}, {
			"id": "learn_more_text_1",
			"order": 2,
			"controlType": "infoblock",
			"content": "To find the deployment error, follow the instructions <a href='https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-deployment-operations'>here</a>."
		}, {
			"id": "resize_determination",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Are you unable to select or deploy the size that you want for your virtual machine?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "true",
					"text": "Yes"
				}, {
					"value": "false",
					"text": "No"
				}, {
					"value": "unknown",
					"text": "I don't know"
				}
			],
			"required": false
		}, {
			"id": "learn_more_text_2",
			"order": 4,
			"controlType": "infoblock",
			"content": "For deployment failures due to quota issues, learn how to <a href='https://docs.microsoft.com/azure/azure-supportability/resource-manager-core-quotas-request'>request additional quota</a><br>Size not available?  Learn how to <a href='https://docs.microsoft.com/azure/azure-supportability/sku-series-unavailable'>request access to specific sizes</a>."
		}, {
			"id": "customimage_determination",
			"order": 5,
			"controlType": "dropdown",
			"displayLabel": "What type of image are you trying to deploy?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Marketplace",
					"text": "Marketplace"
				}, {
					"value": "Generalized",
					"text": "Generalized"
				}, {
					"value": "Specialized",
					"text": "Specialized"
				}, {
					"value": "unknown",
					"text": "I don't know"
				}
			],
			"required": false
		}, {
			"id": "learn_more_text_3",
			"order": 6,
			"controlType": "infoblock",
			"content": "Learn more about <a href='https://docs.microsoft.com/azure/virtual-machines/windows/prepare-for-upload-vhd-image?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json'>creating and uploading images to Azure</a> and <a href='https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-generalize-vhd'>generalized images</a>."
		}, {
			"id": "clone_determination",
			"order": 7,
			"controlType": "dropdown",
			"displayLabel": "Are you trying to clone or duplicate your resource?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "true",
					"text": "Yes"
				}, {
					"value": "false",
					"text": "No"
				}, {
					"value": "unknown",
					"text": "I don't know"
				}
			],
			"required": false
		}, {
			"id": "learn_more_text_4",
			"order": 8,
			"controlType": "infoblock",
			"content": "Read more about best practices for <a href='https://docs.microsoft.com/azure/virtual-machines/capture-image-resource'>cloning a virtual machine</a>."
		}, {
			"id": "additional_details",
			"order": 9,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide these details",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Any portal screenshots that may help us diagnose the issue."
				}, {
					"text": "Specific error that you are experiencing for the failed deployment."
				}, {
					"text": "The expected number, specific size, and region desired, of virtual machines."
				}, {
					"text": "Image name that you are trying to deploy."
				}
			]
		}, {
			"id": "learn_more_text_5",
			"order": 10,
			"controlType": "infoblock",
			"content": "<a href='https://docs.microsoft.com/azure/virtual-machines/windows/troubleshoot-deployment-new-vm'>Learn more</a> about common deployment issues"
		}
	]
}
---
