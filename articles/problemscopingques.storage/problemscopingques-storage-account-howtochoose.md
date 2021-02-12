<properties
	pageTitle="Help with choosing an account type"
	description="Help with choosing storage account type"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32688877"
	productPesIds="15629"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="FECE3A7B-B31A-4E14-81C4-BCE468175A11"
	ownershipId="StorageMediaEdge_AccountManagement"
/>
# Help with choosing an account type
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "formElements": [
        {
            "id": "new_replication",
            "order": 0,
            "controlType": "multiselectdropdown",
            "displayLabel": "New replication type",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "native_file",
                    "text": "Lift and shift an application to the cloud which already uses the native file system APIs to share data between it and other applications running in Azure"
                },
                {
                    "value": "multi_vm_access",
                    "text": "Store development and debugging tools that need to be accessed from many virtual machines"
                },
                {
                    "value": "streaming",
                    "text": "Application to support streaming and random access scenarios"
                },
                {
                    "value": "big_data",
                    "text": "Build an enterprise data lake on Azure and perform big data analytics"
                },
                {
                    "value": "disk_persistent",
                    "text": "Lift and shift applications that use native file system APIs to read and write data to persistent disks"
                },
                {
                    "value": "disk_attached",
                    "text": "Store data that is not required to be accessed from outside the virtual machine to which the disk is attached"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "data_size",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Estimated data size to migrate",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "under50GB",
                    "text": "Under 50 GB"
                },
                {
                    "value": "50GB_100GB",
                    "text": "50 GB - 100 GB"
                },
                {
                    "value": "100GB_1TB",
                    "text": "100 GB - 1 TB"
                },
                {
                    "value": "1TB_50TB",
                    "text": "1 TB - 50 TB"
                },
                {
                    "value": "50TB_100TB",
                    "text": "50 TB - 100 TB"
                },
                {
                    "value": "100TB_500TB",
                    "text": "100 TB - 500 TB"
                },
                {
                    "value": "500TB_1PB",
                    "text": "500 TB - 1 PB"
                },
                {
                    "value": "1PB_5PB",
                    "text": "1 PB - 5 PB"
                },
                {
                    "value": "over5PB",
                    "text": "Greater than 5 PB"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know or not listed above"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
