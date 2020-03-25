<properties
    pageTitle="Azure Stack alert"
    description="Azure Stack alert"
    authors="alexsmithMSFT"
    ms.author="alexsmit, mquian, v-miegge"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32630572,32629199,32629201,32630573,32629220,32629221,32629224,32629237,32629241,32629256,32629267,32629266,32629270"
    productPesIds="16226"
    cloudEnvironments="Public, Fairfax"
    schemaVersion="1"
    articleId="b4b6273d-558e-4f2d-9632-36a830ea0098"
    ownershipId="StorageMediaEdge_AzureStack_Hub"
/>
# Azure Stack alert
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Azure Stack alert",
    "fileAttachmentHint": "To help the support agent identify your issue, please collect and upload the output of Test-AzureStack, Get-AzureStackStampInformation, and/or Azure Stack seed ring logs by following the steps to <a href='https://docs.microsoft.com/azure/azure-stack/azure-stack-diagnostic-test'>Run a validation test for Azure Stack</a>",
    "formElements": [
{
            "id": "hardware_partner",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Azure Stack hardware partner",
            "watermarkText": "Azure Stack OEM Name",
            "dropdownOptions": [
                {
                    "value": "Avanade",
                    "text": "Avanade"
                },
                {
                    "value": "Cisco",
                    "text": "Cisco"
                },
                {
                    "value": "Dell-EMC",
                    "text": "Dell-EMC"
                },
                {
                    "value": "Fujitsu",
                    "text": "Fujitsu"
                },
                {
                    "value": "HPE",
                    "text": "HPE"
                },
                {
                    "value": "Huawei",
                    "text": "Huawei"
                },
                {
                    "value": "Lenovo",
                    "text": "Lenovo"
                },
                {
                    "value": "Terra",
                    "text": "Terra"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false,
            "infoBalloonText": "Choose the partner or OEM for the hardware your Azure Stack stamp is running on"
        },
        {
            "id": "patch_level",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Current Patch Level",
            "watermarkText": "Example: 2002 if your build number is 1.2002.0.35.",
            "dropdownOptions": [
                {
                    "value": "2002",
                    "text": "2002"
                },
                {
                    "value": "1910",
                    "text": "1910"
                },
                {
                    "value": "1908",
                    "text": "1908"
                },
                {
                    "value": "1907",
                    "text": "1907"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false,
            "infoBalloonText": "Example: Select 1903 if your build number is 1.1903.0.35."
        },
        {
            "id": "build_number",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Current Build Number",
            "watermarkText": "Example: 1.1903.0.35",
            "required": false,
            "infoBalloonText": "Includes hotfixes. Learn how to <a href='https://docs.microsoft.com/azure-stack/operator/azure-stack-apply-updates#determine-the-current-version'>determine the current build number</a>"
        },
        {
            "id": "connected_deployment",
            "visibility": "patch_level == 2002",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Can Azure Stack Hub connect to Azure?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [{
                    "value": "Yes",
                    "text": "Yes"
                },{
                    "value": "No",
                    "text": "No"
                },{
                    "value": "dont_know_answer",
                    "text": "Unsure"
                }
            ],
            "required": true
        },
        {
            "id": "cloud_id",
            "visibility": "connected_deployment == Yes",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Enter your the Cloud Stamp ID",
            "watermarkText": "Enter the Stamp Cloud ID",
            "infoBalloonText": "Learn how to <a href='https://docs.microsoft.com/azure-stack/operator/azure-stack-diagnostic-log-collection-overview'>find your Cloud Stamp ID</a>",
            "required": true
        },
        {
            "id": "region_name",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Region Name",
            "watermarkText": "Name of your Azure Stack region",
            "required": false,
            "infoBalloonText": "If you have more than one Azure Stack environment, Ex: REGION from https://adminportal.REGION.FQDN"
        },
        {
            "id": "tenant_impact",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "Availability of running tenant applications impacted",
            "watermarkText": "Tenant impact",
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
            "required": false,
            "infoBalloonText": "Choose yes if availability of running tenant applications has been impacted"
        },
        {
            "id": "alert_name",
            "order": 8,
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
            "order": 9,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 10,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
