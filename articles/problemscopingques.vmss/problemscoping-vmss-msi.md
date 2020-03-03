<properties
                pageTitle="Management"
                description="Management"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32604337"
                productPesIds="16080"
                cloudEnvironments="Public, Fairfax"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0109"
	ownershipId="Compute_VirtualMachineScaleSets"
/>
# Management
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Managed Service Identity (MSI) Integration",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "object_id",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Object ID of the MSI service principal",
            "required": false
        },
        {
            "id": "application_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Application ID of the MSI service principal",
            "required": false
        },
        {
            "id": "vm_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "VM name whether the Object ID of the MSI Service principal is added",
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
