<properties
                pageTitle="Connectivity"
                description="Connectivity"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32553316,32565484"
                productPesIds="13185"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0115"
	ownershipId="Compute_CloudServices_Content"
/>
# Connectivity
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Unable to connect using RDP",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "disable_reenable",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Have you tried to disable and re-enable RDP from the Azure portal?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        },
        {
            "id": "able_operation",
            "order": 2,
            "controlType": "multiselectdropdown",
            "displayLabel": "Which of the following are you able to do?",
            "watermarkText": "Choose all that apply.",
            "dropdownOptions": [
                {
                    "value": "RDP to other VMs or Cloud Services from your network",
                    "text": "RDP to other VMs or Cloud Services from your network"
                },
                {
                    "value": "RDP to an Azure VM (IaaS or PaaS) and then RDP from there to the target cloud service",
                    "text": "RDP to an Azure VM (IaaS or PaaS) and then RDP from there to the target cloud service"
                },
                {
                    "value": "RDP from another network (i.e, outside of your corporate network) such as home, tethering, coffee shop wifi, etc.",
                    "text": "RDP from another network (i.e, outside of your corporate network) such as home, tethering, coffee shop wifi, etc."
                }
            ],
            "required": false
        },
        {
            "id": "if_partofvnet",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is this Cloud Service part of a vnet?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        },
        {
            "id": "vnet_tried",
            "order": 4,
            "visibility": "if_partofvnet == Yes",
            "controlType": "multiselectdropdown",
            "displayLabel": "Which of the following have you tried",
            "watermarkText": "Choose all that apply",
            "dropdownOptions": [
                {
                    "value": "RDP from a VM within the same VNET",
                    "text": "RDP from a VM within the same VNET"
                },
                {
                    "value": "Remove Cloud Services from VNET",
                    "text": "Remove Cloud Services from VNET"
                },
                {
                    "value": "Create rules that allow traffic on ports 3389 and 20000",
                    "text": "Create rules that allow traffic on ports 3389 and 20000"
                },
                {
                    "value": "None of the above",
                    "text": "None of the above"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
