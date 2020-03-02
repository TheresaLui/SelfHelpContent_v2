<properties
	pageTitle="Storage Firewall and VNet"
	description="Storage Firewall and VNet scoping question"
	authors="AngshumanNayakMSFT"
	ms.author="annayak"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32682428,32682429,32682430,32682433,32682434,32682435,32682438,32682439,32682440,32682443,32682444,32682445"
	productPesIds="15629,16459,16462,16461,16598"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest"
	schemaVersion="1"
	articleId="StorageScoping_all_firewall_Vnet"
/>
# Storage Firewall and VNet

---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Storage Firewall and VNet scoping question",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Firewall & VNet Issues Troubleshooter",
        "description": "If you are reporting about an issue please help us with a few inputs and give us couple of minutes to run automated diagnostics. We can help diagnose your problem without the need of opening a support ticket.",
        "insightNotAvailableText": "Our automated troubleshooter did not detect any issues with your resource. You can help us by providing the right inputs below and ensuring that the format is as suggested in the watermark."
    },
    "formElements": [
        {

            "id": "connection_topology_dropdown",
            "visibility": "null",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Where is the connection source located?",
            "watermarkText": "Choose the appropriate topology",
            "dropdownOptions": [
                {
                    "value": "On_Azure_Cloud",
                    "text": "On Azure Cloud"
                },
                {
                    "value": "On_Premise",
                    "text": "On Premise"
                },
                {
                    "value": "dont_know_answer",
                    "text": "On Non-Azure Cloud"
                }
            ],
            "required": true
        },
        {

           "id": "service_provider_selection_dropdown",
            "order": 5,
            "visibility": "connection_topology_dropdown == On_Azure_Cloud",
            "controlType": "dropdown",
            "displayLabel": "Azure Service",
            "watermarkText": "Select the Azure Service Type",
            "dropdownOptions": [
                {
                    "value": "cloud_services",
                    "text": "Cloud Services (Web roles/Worker roles) "
                },
                {
                    "value": "container_services_instances_registries",
                    "text": "Container Services, Instances and Registries"
                },
                {
                    "value": "databases",
                    "text": "Databases"
                },
                {
                    "value": "data_and_analytics",
                    "text": "Data and Analystics "
                },
                {
                    "value": "monitoring_management",
                    "text": "Monitoring and Management "
                },
                {
                    "value": "networking",
                    "text": "Networking"
                },
                {
                    "value": "virtual_machine",
                    "text": "Virtual Machine [including SQL Virtual Manchines]"
                },
                {
                    "value": "virtual_machine_scalesets",
                    "text": "Virtual Machine Scale Sets"
                },
                {
                    "value": "web_function_mobile_app",
                    "text": "Web, Function & Mobile App"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not listed above"
                }
            ],
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {

           "id": "resourcetype_virtualmachine_selection_dropdown",
            "order": 6,
            "visibility": "service_provider_selection_dropdown == virtual_machine",
            "controlType": "dropdown",
            "displayLabel": "Virtual Machine Type",
            "watermarkText": "Select the appropriate Virtual Machine Type",
            "dropdownOptions": [
                {
                    "value": "MICROSOFT.COMPUTE/VIRTUALMACHINES",
                    "text": "ARM Virtual Machines"
                },
                {
                    "value": "MICROSOFT.CLASSICCOMPUTE/VIRTUALMACHINES",
                    "text": "Classic Virtual Machines"
                },
                {
                    "value": "Microsoft.SqlVirtualMachine/sqlVirtualMachines",
                    "text": "SQL Virtual Machines"
                },
               {
                    "value": "dont_know_answer",
                    "text": "Not listed above"
                }
            ],
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },

        {

           "id": "resource_list_virtualmachine",
            "order": 10,
            "visibility": "resourcetype_virtualmachine_selection_dropdown != null && resourcetype_virtualmachine_selection_dropdown != dont_know_answer",
            "controlType": "dropdown",
            "displayLabel": "Select the connection source",
            "watermarkText": "Filter by name",
            "dynamicDropdownOptions": {
                "uri":"subscriptions/{subscriptionId}/resources?api-version=2019-10-01&$filter=resourceType eq 'Microsoft.Compute/virtualMachines",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other or none of the above"
                }
            }

        },
        {

           "id": "resourceGroup_list",
            "order": 40,
            "visibility": "connection_topology_dropdown == On_Azure_Cloud",
            "controlType": "dropdown",
            "displayLabel": "Select the Resource Group of the source",
            "watermarkText": "Filter by name",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/resourcegroups?api-version=2018-05-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other or none of the above"
                }
            }

        },

       {
            "id": "resourceProvider_list",
            "order": 60,
            "visibility": "resourceGroup_list != null",
            "controlType": "dropdown",
            "displayLabel": "Select the type of resoure",
            "watermarkText": "Filter by name",
            "dynamicDropdownOptions": {
                "dependsOn": "resourceGroup_list",
                "uri": "/subscriptions/{subscriptionId}/providers?api-version=2019-10-01",
                "jTokenPath": "value",
                "textProperty": "namespace",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
		"valuePropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other or none of the above"
                }
            },
            "DropdownOptions": [
                {
                    "value": "Unable to retrieve list of resource providers",
                    "text": "Unable to retrieve list of resources providers"
                }
            ]

        },
        {
            "id": "resourceName_list",
            "order": 100,
            "visibility": "resourceProvider_list != null",
            "controlType": "dropdown",
            "displayLabel": "Select the name of the source",
            "watermarkText": "Filter by name",
            "dynamicDropdownOptions": {
                "dependsOn": "resourceProvider_list",
                "uri": "/subscriptions/{subscriptionId}/resourceGroups/ATMtestRG/resources?api-version=2019-10-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
		"valuePropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other or none of the above"
                }
            },
            "DropdownOptions": [
                {
                    "value": "Unable to retrieve list of resources",
                    "text": "Unable to retrieve list of resources"
                }
            ]

        },
        {
            "id": "problem_start_time",
            "order": 1000,
            "controlType": "datetimepicker",
            "displayLabel": "Select time (in local time zone) of the most recent occurrence",
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "error_code_dropdown",
            "order": 2000,
            "controlType": "dropdown",
            "displayLabel": "Error code",
            "watermarkText": "HTTP error of failed operation",
            "dropdownOptions": [
                {
                    "value": "HTTP_400",
                    "text": "HTTP 400"
                },
                {
                    "value": "HTTP_403",
                    "text": "HTTP 403"
                },
                {
                    "value": "HTTP_404",
                    "text": "HTTP 404"
                },
                {
                    "value": "HTTP_409",
                    "text": "HTTP 409"
                },
                {
                    "value": "HTTP_500",
                    "text": "HTTP 500"
                },
                {
                    "value": "HTTP_501",
                    "text": "HTTP 501"
                },
                {
                    "value": "HTTP_502",
                    "text": "HTTP 502"
                },
                {
                    "value": "HTTP_503",
                    "text": "HTTP 503"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not listed above"
                }
            ],
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "request_id",
            "order": 3000,
            "controlType": "textbox",
            "displayLabel": "Storage server Request ID",
            "watermarkText": "Request ID of failed operation ending with 000000",
            "textPropertyRegex": "^([0-9A-Za-z]{8}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{6}[0]{6})$",
            "required": false,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "problem_description",
            "order": 4000,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "learn_more_text",
            "order": 7000,
            "controlType": "infoblock",
            "content": "You can follow our guideline to <a href='https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting'>monitor, diagnose, and troubleshoot Microsoft Azure Storage</a> issues."
        }
    ],
    "$schema": "SelfHelpContent"
}
---
