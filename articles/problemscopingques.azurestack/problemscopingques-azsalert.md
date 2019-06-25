<properties
    pageTitle="Azure Stack alert"
    description="Azure Stack alert"
    authors="TobyTu"
    ms.author="prchint"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32630572,32629199,32629201,32630573,32629220,32629221,32629224,32629237,32629241,32629256,32629267,32629266,32629270"
    productPesIds="16226"
    cloudEnvironments="Public"
    schemaVersion="1"
    articleId="b4b6273d-558e-4f2d-9632-36a830ea0098"
/>
# Azure Stack alert
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Azure Stack alert",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "alert_name",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Alert name: ",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "A physical disk has failed",
                    "text": "A physical disk has failed"
                },
                {
                    "value": "A physical disk is quarantined because it is not supported",
                    "text": "A physical disk is quarantined because it is not supported"
                },
                {
                    "value": "A physical disk is quarantined because its firmware version is not supported",
                    "text": "A physical disk is quarantined because its firmware version is not supported"
                },
                {
                     "value": "A replacement disk has existing data and is quarantined",
                     "text": "A replacement disk has existing data and is quarantined"
                },
                {
                     "value": "Account and Container Service data corruption",
                     "text": "Account and Container Service data corruption"
                },
                {
                     "value": "Azure Stack update stopped with errors",
                     "text": "Azure Stack update stopped with errors"
                },
                {
                     "value": "Backup could not be deleted",
                     "text": "Backup could not be deleted"
                },
                {
                     "value": "Backup failed because backup file share path is not valid",
                     "text": "Backup failed because backup file share path is not valid"
                },
                {
                     "value": "Backup failed because cannot access backup share",
                     "text": "Backup failed because cannot access backup share"
                },
                {
                     "value": "Backup failed because file share is full",
                     "text": "Backup failed because file share is full"
                },
                {
                     "value": "Backup failed because of an unknown error",
                     "text": "Backup failed because of an unknown error"
                },
                {
                     "value": "Backup failed during file copy to external share",
                     "text": "Backup failed during file copy to external share"
                },
                {
                     "value": "Backup file share is not accessible",
                     "text": "Backup file share is not accessible"
                },
                {
                     "value": "Backup is not enabled for a location",
                     "text": "Backup is not enabled for a location"
                },
                {
                     "value": "Backup only partially completed because of an unexpected error",
                     "text": "Backup only partially completed because of an unexpected error"
                },
                {
                     "value": "Blob service errors",
                     "text": "Blob service errors"
                },
                {
                     "value": "BMC connection timeout",
                     "text": "BMC connection timeout"
                },
                {
                     "value": "Cannot write to the backup file share",
                     "text": "Cannot write to the backup file share"
                },
                {
                     "value": "Connectivity has been lost to a physical disk",
                     "text": "Connectivity has been lost to a physical disk"
                },
                {
                     "value": "Failed attempt to update firmware on a physical disk",
                     "text": "Failed attempt to update firmware on a physical disk"
                },
                {
                     "value": "File share to volume mapping lost",
                     "text": "File share to volume mapping lost"
                },
                {
                     "value": "Health controller cannot access storage account",
                     "text": "Health controller cannot access storage account"
                },
                {
                     "value": "Infrastructure backup settings need to be updated",
                     "text": "Infrastructure backup settings need to be updated"
                },
                {
                     "value": "Infrastructure backups are paused",
                     "text": "Infrastructure backups are paused"
                },
                {
                     "value": "Infrastructure role instance is unavailable",
                     "text": "Infrastructure role instance is unavailable"
                },
                {
                     "value": "Infrastructure role is unhealthy",
                     "text": "Infrastructure role is unhealthy"
                },
                {
                     "value": "Infrastructure role is unresponsive",
                     "text": "Infrastructure role is unresponsive"
                },
                {
                     "value": "Invalid BMC credentials",
                     "text": "Invalid BMC credentials"
                },
                {
                     "value": "Invalid OEM activation BIOS marker",
                     "text": "Invalid OEM activation BIOS marker"
                },
                {
                     "value": "Low disk space for Azure Stack infrastructure",
                     "text": "Low disk space for Azure Stack infrastructure"
                },
                {
                     "value": "Low memory capacity",
                     "text": "Low memory capacity"
                },
                {
                     "value": "Missing OEM activation BIOS marker",
                     "text": "Missing OEM activation BIOS marker"
                },
                {
                     "value": "Missing OEM activation license file",
                     "text": "Missing OEM activation license file"
                },
                {
                     "value": "Network interface disconnected",
                     "text": "Network interface disconnected"
                },
                {
                     "value": "Node inaccessible for virtual machine placement",
                     "text": "Node inaccessible for virtual machine placement"
                },
                {
                     "value": "Node not connected to network controller",
                     "text": "Node not connected to network controller"
                },
                {
                     "value": "Pending external certificate expiration",
                     "text": "Pending external certificate expiration"
                },
                {
                     "value": "Public IP address utilization at 100% across all pools",
                     "text": "Public IP address utilization at 100% across all pools"
                },
                {
                     "value": "Public IP address utilization at 90% across all pools",
                     "text": "Public IP address utilization at 90% across all pools"
                },
                {
                     "value": "Public IP address utilization at 70% across all pools",
                     "text": "Public IP address utilization at 70% across all pools"
                },
                {
                     "value": "Queue service errors",
                     "text": "Queue service errors"
                },
                {
                     "value": "Resource Provider does not process ARM requests",
                     "text": "Resource Provider does not process ARM requests"
                },
                {
                     "value": "Route publication failure",
                     "text": "Route publication failure"
                },
                {
                     "value": "Scale unit node is offline",
                     "text": "Scale unit node is offline"
                },
                {
                     "value": "Sharing is not accessible",
                     "text": "Sharing is not accessible"
                },
                {
                     "value": "Storage device failure",
                     "text": "Storage device failure"
                },
                {
                     "value": "Storage Resource Provider infrastructure or dependencies is not available",
                     "text": "Storage Resource Provider infrastructure or dependencies is not available"
                },
                {
                     "value": "Storage Resource Provider internal data store is unavailable",
                     "text": "Storage Resource Provider internal data store is unavailable"
                },
                {
                     "value": "Table service errors",
                     "text": "Table service errors"
                },
                {
                     "value": "The backup file share is almost full",
                     "text": "The backup file share is almost full"
                },
                {
                     "value": "The blob service cannot attach to a file share",
                     "text": "The blob service cannot attach to a file share"
                },
                {
                     "value": "The scheduled backup was skipped due to a conflict with unfinished operations",
                     "text": "The scheduled backup was skipped due to a conflict with unfinished operations"
                },
                {
                     "value": "Unable to connect to the remote service",
                     "text": "Unable to connect to the remote service"
                },
                {
                     "value": "Unable to connect to UsageBridgeStore",
                     "text": "Unable to connect to UsageBridgeStore"
                },
                {
                     "value": "Unable to provision virtual machines for specific class and size due to low memory capacity",
                     "text": "Unable to provision virtual machines for specific class and size due to low memory capacity"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
