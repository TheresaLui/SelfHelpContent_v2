<properties
                pageTitle="Configuration and Setup"
                description="Configuration and Setup"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32615272"
                productPesIds="16080"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0105"
	ownershipId="Compute_VirtualMachineScaleSets_Content"
/>
# Config and Setup
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Unable to Create Shared Gallery, Image Definition or Image Version",
    "diagnosticCard": {
            "title": "Virtual machine scale set diagnostics",
            "description": "These diagnostics will check for details about your selected VM instance within your VMSS.",
            "insightNotAvailableText": "We didn't find any problems"},
    "formElements": [
        {
            "id": "vmss_instance",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "If your issue is related to a specific instance, select the instance name",
            "dynamicDropdownOptions": {
                "uri": "{resourceId}/virtualMachines?api-version=2019-03-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
            "dropdownOptions": [
                {
                    "value": "Unable to retrieve list of instances.",
                    "text": "Unable to retrieve list of instances."
                }
            ],
            "useAsAdditionalDetails": false,
            "required": false,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "configsetup_create",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What are you trying to create?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Shared Image Gallery",
                    "text": "Shared Image Gallery"
                },
                {
                    "value": "Image Definition",
                    "text": "Image Definition"
                },
                {
                    "value": "Image Version",
                    "text": "Image Version"
                }
            ],
            "required": false
        },
        {
            "id": "imageversion_location",
            "order": 3,
            "visibility": "configsetup_create == Image Version",
            "controlType": "dropdown",
            "displayLabel": "Is the source image in the same location as the image version?",
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
            "id": "imageversion_ostype",
            "order": 4,
            "visibility": "configsetup_create == Image Version",
            "controlType": "dropdown",
            "displayLabel": "Does the OSType of the source image match the image definition?",
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
            "id": "imageversion_replication",
            "order": 5,
            "visibility": "configsetup_create == Image Version",
            "controlType": "dropdown",
            "displayLabel": "Has the replication of the image version to all target regions been completed?",
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
            "id": "imageversion_datadisk",
            "order": 6,
            "visibility": "configsetup_create == Image Version",
            "controlType": "dropdown",
            "displayLabel": "Does your image have a data disk of more than 1TB?",
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
            "id": "resource_name",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the name of the resource (e.g., image version, gallery1/image1/1.0.0)",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_description",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": false,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 9,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
