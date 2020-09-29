<properties
                pageTitle="Virtual Disk Management"
                description="Virtual Disk Management"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32632139"
                productPesIds="14749,15571,15797,16454,16470"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0072"
	ownershipId="Compute_VirtualMachines_Content"
/>
# Virtual Disk Management
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Attaching or detaching virtual disks",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "virtualdisk_attachdetach",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Are you trying to attach or detach a virtual disk?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Attach",
                    "text": "Attach"
                },
                {
                    "value": "Detach",
                    "text": "Detach"
                }
            ],
            "required": false
        },
        {
            "id": "virtualdisk_ifnew",
            "order": 2,
            "visibility": "virtualdisk_attachdetach == Attach",
            "controlType": "dropdown",
            "displayLabel": "Are you attaching a new data disk or an existing data disk?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "A new data disk",
                    "text": "A new data disk"
                },
                {
                    "value": "An existing data disk",
                    "text": "An existing data disk"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
