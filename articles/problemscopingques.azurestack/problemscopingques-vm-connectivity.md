<properties
    pageTitle="Azure Stack virtual machine connectivity"
    description="Azure Stack virtual machine connectivity"
    authors="TobyTu"
    ms.author="prchint"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32629202"
    productPesIds="16226"
    cloudEnvironments="Public"
    schemaVersion="1"
    articleId="b4b6273d-9542-4f2d-5238-36a830ea6398"
/>
# Azure Stack virtual machine connectivity questions
---
{
  "subscriptionRequired": true,
  "resourceRequired": false,
  "title": "Azure Stack virtual machine connectivity",
  "fileAttachmentHint": "",
  "formElements": [{
            "id": "vm_status",
            "order": 1,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Examine the boot diagnostics and image snapshot, is the VM booted and running?",
            "watermarkText": "",
            "required": false
		},{
            "id": "destination_name",
            "order": 2,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "What is the destination URL or IP address and/or port that you are connecting to?",
            "watermarkText": "",
            "required": false
		},{
            "id": "connect_name",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "If destination endpoint is within Azure Stack, what are you connecting to?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Private IP address of VM or load balancer (ILB)",
                    "text": "Private IP address of VM or load balancer (ILB)"
                },
                {
                    "value": "Public IP address of VM or load balancer",
                    "text": "Public IP address of VM or load balancer"
                }
            ],
            "required": false
        },{
            "id": "connect_method",
            "order": 4,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Are you attempting to connect through S2S tunnel or does the VNet have a Virtual Network Gateway deployed?",
            "watermarkText": "",
            "required": false
		},{
            "id": "source_ip",
            "order": 5,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "What is the source IP address that you are attempting to connect from?",
            "watermarkText": "",
            "required": false
		},{
			"id": "problem_start_time",
			"order": 6,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "problem_description",
			"order": 7,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": []
		}
	],
  "$schema": "SelfHelpContent"
}
---