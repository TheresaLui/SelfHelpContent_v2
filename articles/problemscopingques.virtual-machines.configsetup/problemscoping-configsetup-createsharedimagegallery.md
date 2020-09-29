<properties
                pageTitle="Configuration and Setup"
                description="Configuration and Setup"
                authors="summertgu"
                ms.author="tiag, sischleg"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32615272"
                productPesIds="14749,15571,15797,16454,16470"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0079"
	ownershipId="Compute_VirtualMachines_Content"
/>
# Config and Setup
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Unable to Create Shared Gallery, Image Definition or Image Version",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "configsetup_create",
            "order": 1,
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
            "order": 2,
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
            "order": 3,
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
            "order": 4,
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
            "order": 5,
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
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the name of the resource (e.g., image version, gallery1/image1/1.0.0)",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": false,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 8,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
