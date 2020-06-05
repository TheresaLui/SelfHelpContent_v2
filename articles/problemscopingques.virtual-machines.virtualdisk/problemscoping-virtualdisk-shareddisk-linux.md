<properties
                pageTitle="Virtual Disk Management"
                description="Virtual Disk Management"
                authors="timbasham"
                ms.author="tibasham"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32740057"
                productPesIds="15571,15797,16454,16470"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="68c49447-7c8c-4a84-ad7a-4e5fd1dcbe6b"
	ownershipId="Compute_VirtualMachines"
/>
# Virtual Disk Management
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Issue with shared disks",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "virtualdisk_proximityplacementgroups",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Are all of the VMs sharing the disk in the same proximity placement group?",
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
            "id": "virtualdisk_availabilityset",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are your VMs in an availability set or a VM Scale Set?",
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
            "id": "virtualdisk_faultdomain",
            "order": 3,
            "visibility": "virtualdisk_availabilityset == Yes",
            "controlType": "dropdown",
            "displayLabel": "Are you using a fault domain count of 1 in your availability set or scale set?",
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
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
