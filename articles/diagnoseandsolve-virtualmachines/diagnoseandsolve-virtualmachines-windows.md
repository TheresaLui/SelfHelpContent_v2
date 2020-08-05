<properties
pageTitle="Top common problems for compute"
description="Menu based workflow document for top compute problems"        
service="microsoft.compute"
resource="virtualmachines"
authors="gansmore,summertgu"
ms.author="ganesh.more,tiag"
displayOrder=""
articleId="202605d3-432d-4799-85df-a35504c94b5f"
selfHelpType="diagnoseandsolve"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public, Fairfax, usnat, ussec"
ownershipId="Compute_VirtualMachines_Content"
/>
# Diagnose and solve v2 test article for windows
---
{
	"$schema":"SelfHelpContent",
  "commonProblems": [
	{
		"id": "Cannot_Connect_to_VM",
		"title": "Cannot Connect to VM",
		"description": "Troubleshoot connectivity issues with an Azure VM",
		"category": "Connectivity",
		"searchTags": "connect, connectivity, test, rdp, ssh, port, access, server, public ip, application, firewall, linux, disable, ping, login",
		"supportTopicId": "",
		"subProblems": [
			{
				"id": "Configuration_change_impacted_connectivity",
				"title": "Configuration change impacted connectivity",
				"description": "Troubleshoot connectivity issues due to configuration changes",
				"supportTopicId": "32615530",
				"commonSolutionArticleId": "b53b4761-a678-45ea-8869-24973e5a6678",
				"symptomId": ""
			},
			{
				"id": "Troubleshoot_network_security_group",
				"title": "Troubleshoot network security group (NSG)",
				"description": "Troubleshoot connectivity issues due to network security group rules",
				"supportTopicId": "32615530",
				"commonSolutionArticleId": "c5ccfcb5-7f2c-47d9-bc8b-46b6beab5480",
				"symptomId": ""
			},
			{
				"id": "Troubleshoot_VM_firewall",
				"title": "Troubleshoot VM firewall",
				"description": "Troubleshoot connectivity issues due to firewall rules",
				"supportTopicId": "32615534",
				"commonSolutionArticleId": "72a1d281-9123-421c-9cf6-90fed2618648",
				"symptomId": ""
			},
			{
				"id": "Public_IP_issue",
				"title": "Public IP issue",
				"description": "Troubleshoot connectivity issues due to Public IP issues",
				"supportTopicId": "32615527",
				"commonSolutionArticleId": "6ce39c44-2a32-41c2-a8ce-7dedc93e6619",
				"symptomId": ""
			},
			{
				"id": "Serial_console_access",
				"title": "Serial console access",
				"description": "Understand how to use serial console to troubleshoot connectivity issues",
				"supportTopicId": "32615528",
				"commonSolutionArticleId": "12572186-90fb-4c0e-94f6-45522bd8bf64",
				"symptomId": ""
			},
			{
				"id": "Cannot_RDP",
				"title": "Cannot RDP",
				"description": "Troubleshoot connectivity issues to an Azure virtual machine",
				"supportTopicId": "32615526",
				"commonSolutionArticleId": "d67fb475-a831-4f4b-a6ce-7fbacb0bf9df",
				"symptomId": ""
			}
		]
	},
	{
      "id": "VM_Performance_Issues",
      "title": "VM Performance Issues",
      "description": "Troubleshoot issues that cause low performance of an Azure VM",
      "category": "Performance",
      "searchTags": "slow, performance, disk, server, cpu, network, high, memory, size, time, usage, latency, gpu, resize, throughput, premium, iop, ssd, sql, data, storage",
      "supportTopicId": "",
      "subProblems": [
        {
          "id": "Disk_throughput_low",
          "title": "Disk throughput or IOPS are lower than expected",
          "description": "Troubleshoot performance issues when disk throughput is lower than expected",
          "supportTopicId": "32628264",
          "commonSolutionArticleId": "1846ef6d-3aa8-44c1-bff0-cc8ede1933c6",
          "symptomId": ""
        },
        {
          "id": "CPU_usage_high",
          "title": "CPU usage is higher than expected",
          "description": "Troubleshoot performance issues when CPU usage is higher than expected",
          "supportTopicId": "32628261",
          "commonSolutionArticleId": "c56d711a-2df1-4c2a-b250-b6dc68a4975b",
          "symptomId": ""
        },
        {
          "id": "Memory_usage_high",
          "title": "Memory usage is higher than expected",
          "description": "Troubleshoot performance issues when memory usage is higher than expected",
          "supportTopicId": "32628275",
          "commonSolutionArticleId": "6aaf31c5-6dde-4418-9af0-f3fa234593fc",
          "symptomId": ""
        },
        {
          "id": "GPU_processing_slow",
          "title": "GPU processing is slower than expected",
          "description": "Troubleshoot performance issues when GPU processing is slower than expected",
          "supportTopicId": "32628268",
          "commonSolutionArticleId": "0ab4f15c-3ab7-44d1-8f36-f81b3156971b",
          "symptomId": ""
        },
        {
          "id": "Unable_to_resize_my_VM",
          "title": "Unable to resize my VM",
          "description": "Unable to resize Azure VMs",
          "supportTopicId": "32690776",
          "commonSolutionArticleId": "e7920c6e-0eec-4a8f-876d-280f5d4d1035",
          "symptomId": ""
        }
      ]
    },
    {					   
      "id": "Troubleshoot_Deployment_Failures",
      "title": "Troubleshoot Deployment Failures",
      "description": "Troubleshoot failures and errors when creating a new VM in Azure",
      "category": "Deployment",
      "searchTags": "create, image, deploy, deployment, start, quota, size, snapshot, provision, capture, vhd, resource, subscription, time, ARM, network, server, SQL, marketplace, extension, standard, network, operation",
      "supportTopicId": "",
      "subProblems": [
        {
          "id": "Allocation_failure",
          "title": "Allocation failure",
          "description": "Troubleshoot allocation failures when creating a new VM in Azure",
          "supportTopicId": "32628252",
          "commonSolutionArticleId": "9c0b9ec9-a07a-40e3-a6a2-f4d49f5f4ccb",
          "symptomId": ""
        },
        {
          "id": "Captured_or_generalized_image_deployment_failure",
          "title": "Captured or generalized image deployment failure",
          "description": "Troubleshoot issues when creating a managed image of a generalized VM in Azure",
          "supportTopicId": "32628259",
          "commonSolutionArticleId": "759ac937-32e7-4e89-a82c-28287ad85f9e",
          "symptomId": ""
        },
        {
          "id": "Provisioning_or_deployment_timeout_error",
	  "title": "Provisioning or deployment timeout error",
          "description": "Troubleshoot provisioning or deployment timeout errors when creating a new VM in Azure",
          "supportTopicId": "32628279",
          "commonSolutionArticleId": "2b6deeb3-490a-4d18-8a36-83ed65de8451",
          "symptomId": ""
        },
        {
          "id": "ARM_template_error",
          "title": "ARM template error",
          "description": "Troubleshoot issues when deploying with ARM template",
          "supportTopicId": "32628255",
          "commonSolutionArticleId": "91c00640-5896-42ec-9b42-652a3143fd0d",
          "symptomId": ""
        },
        {
          "id": "Custom_image_deployment_failure",
          "title": "Custom image deployment failure",
          "description": "Troubleshoot issues when deploying a custom image",
          "supportTopicId": "32628262",
          "commonSolutionArticleId": "69867902-65a9-4c5a-aa04-91c748bd351d",
          "symptomId": ""
        },
        {
          "id": "Marketplace_image_deployment_failure",
          "title": "Marketplace image deployment failure",
          "description": "Troubleshoot issues when deploying a marketplace image",
          "supportTopicId": "32628274",
          "commonSolutionArticleId": "0bb36f17-2342-4c60-8bcd-e4416a54a9cd",
          "symptomId": ""
        }
      ]
    },
		{
			"id": "Allocation_recommender",
			"title": "Allocation Success Recommender",
			"description": "Provide prediction of the chance of a successful allocation in the next 7 days for given sizes and regions.",
			"category": "Deployment",
			"searchTags": "deploy, deployment, create, allocation, standard, resource, size, region, available, location, instance",
			"supportTopicId": "32743100",
			"commonSolutionArticleId": "37f0fdfb-3b67-4b90-b692-c0db770af827",
			"symptomId": ""
		},
		{
      "id": "VM_Deployment_Guidance",
      "title": "VM Deployment Guidance",
      "description": "Guidance on creating a new VM in Azure",
      "category": "Deployment",
      "searchTags": "deploy, deployment, create, disk, manage, network, image, vhd, server, standard, resource, size, region, available, location",
      "supportTopicId": "",
      "subProblems": [
        {
          "id": "Deploy_with_managed_disks",
          "title": "Deploy with managed disks",
          "description": "Guidance on deploying with managed disks or converting a VM from unmanaged disks to managed disks",
          "supportTopicId": "32628271",
          "commonSolutionArticleId": "f29b946f-107f-4c9d-8574-0014f3c2b8f6",
          "symptomId": ""
        },
        {
          "id": "Prepare_an_image",
          "title": "Prepare an image",
          "description": "Guidance on capturing a VM to image in Azure",
          "supportTopicId": "32628272",
          "commonSolutionArticleId": "a316fb37-cb8c-4b94-bdb1-276b2d90a555",
          "symptomId": ""
        },
        {
          "id": "Choosing_Region_or_VM_size",
          "title": "Choosing Region or VM size",
          "description": "Guidance on creating a new VM in an unavailable size or region, or when finding suitable SKU for deployment",
          "supportTopicId": "32628263",
          "commonSolutionArticleId": "37f0fdfb-3b67-4b90-b692-c0db770af827",
          "symptomId": ""
        }
      ]
    },
    {
      "id": "Help_with_VM_Password_Reset",
      "title": "Help with VM Password Reset",
      "description": "Guidance on resetting the credentials of an existing user or creating a new user",
      "category": "Connectivity",
      "searchTags": "reset, password, connect, connectivity, login, access, root, user, username, rdp, ssh, admin",
      "supportTopicId": "",
      "commonSolutionArticleId": "6c04f1f6-0cfe-4a23-bc8a-1f0c2d59aa56",
      "symptomId": ""
    },
    {
      "id": "VM_is_not_booting",
      "title": "VM is not booting",
      "description": "Troubleshoot common boot errors for non-bootable VMs",
      "category": "Connectivity",
      "searchTags": "stuck, boot, start, fail, server, restart, reboot, update, disk, load, storage, encryption",
      "supportTopicId": "32628284",
      "commonSolutionArticleId": "f77c4d7d-6738-46fb-afea-07b627a597b6",
      "symptomId": ""
    },
    {
      "id": "Allocation_failure_Top",
      "title": "Allocation failure",
      "description": "Troubleshoot allocation failures with a VM in Azure (Start VM or Create VM)",
      "category": "Allocation",
      "searchTags": "allocation",
      "supportTopicId": "32628252",
      "commonSolutionArticleId": "9c0b9ec9-a07a-40e3-a6a2-f4d49f5f4ccb",
      "symptomId": ""
    },
    {
      "id": "Help_with_VM_Sizing_Top",
      "title": "Help with VM Sizing",
      "description": "Guidance on VM sizing and troubleshooting resize issues",
      "category": "Management",
      "searchTags": "resize, size, throughput, performance",
      "supportTopicId": "",
      "subProblems": [
        {
          "id": "Guidance_for_better_VM_sizing_and_throughput",
          "title": "Guidance for better VM sizing and throughput",
          "description": "Guidance on VM sizing and throughput for better performance of Azure VMs",
          "supportTopicId": "32632142",
          "commonSolutionArticleId": "6c90898f-7758-42e3-97bf-d85745fe6c08",
          "symptomId": ""
        },
        {
          "id": "Unable_to_resize_my_VM",
          "title": "Unable to resize my VM",
          "description": "Unable to resize Azure VMs",
          "supportTopicId": "32632142",
          "commonSolutionArticleId": "6c90898f-7758-42e3-97bf-d85745fe6c08",
          "symptomId": ""
        }
      ]
    },
    {
      "id": "Cannot_Start_or_Stop_VM",
      "title": "Cannot Start or Stop VM",
      "description": "Troubleshoot issues when starting or stopping a VM in Azure",
      "category": "Deployment",
      "searchTags": "stuck, start, stop, deallocate, state, restart, unresponsive, status, server, connect, delete, reboot, redeploy, update",
      "supportTopicId": "",
      "subProblems": [
        {
          "id": "Cannot_start_after_configuration_change",
          "title": "Cannot start after configuration change",
          "description": "Troubleshoot VM start issues due to configuration changes",
          "supportTopicId": "32628285",
          "commonSolutionArticleId": "b0380479-ed1b-4df3-b708-e3ebefc4deeb",
          "symptomId": ""
        },
        {
          "id": "Disk_related_error",        
          "title": "Disk related error",
          "description": "Troubleshoot disk related errors when starting a VM in Azure",
          "supportTopicId": "32628265",
          "commonSolutionArticleId": "5a916d8f-c05d-4db6-9787-6b5003a9dd56",
          "symptomId": ""
        },
        {
          "id": "Allocation_failure",
          "title": "Allocation failure",
          "description": "Troubleshoot allocation failures when starting a VM in Azure",
          "supportTopicId": "32628253",
          "commonSolutionArticleId": "9c0b9ec9-a07a-40e3-a6a2-f4d49f5f4ccb",
          "symptomId": ""
        },
        {
          "id": "VM_unresponsive_to_start_or_stop_operations",
          "title": "VM unresponsive to start or stop operations",
          "description": "Troubleshoot issues when VM is not responsive to start or stop operations",
          "supportTopicId": "32628286",
          "commonSolutionArticleId": "8d3e0818-0feb-4207-a953-b89f19198227",
          "symptomId": ""
        },
        {
          "id": "Start_or_stop_operation_failed",
          "title": "Start or stop operation failed",
          "description": "Troubleshoot failures when starting or stopping a VM in Azure",
          "supportTopicId": "32628282",
          "commonSolutionArticleId": "5e8c5760-d46d-4c14-9f30-52eb26ca9538",
          "symptomId": ""
        }
      ]
    },
    {
      "id": "Unexpected_VM_Restart",
      "title": "Unexpected VM Restart",
      "description": "Troubleshoot issues that cause an Azure VM to restart unexpectedly",
      "category": "Management",
      "searchTags": "update, reboot, server, restart, loop, unexpected, patch, application, service",
      "supportTopicId": "",
      "subProblems": [
        {
          "id": "Guest_OS_causing_restarts",
          "title": "Guest OS causing restarts",
          "description": "Troubleshoot VM restart issues caused by issues within the guest operating system",
          "supportTopicId": "32628269",
          "commonSolutionArticleId": "9c823f1b-b821-4c3a-a558-356fb425dec3",
          "symptomId": ""
        },
        {
          "id": "Troubleshoot_Windows_Update_issues",
          "title": "Troubleshoot Windows Update issues",
          "description": "Troubleshoot VM restart issues caused by Windows Update issues",
          "supportTopicId": "32628289",
          "commonSolutionArticleId": "26d21b85-4966-4e96-b29e-0866f17f2bf6",
          "symptomId": ""
        },
        {
          "id": "Request_Root_Cause_for_VM_Restart",
          "title": "Request Root Cause for VM Restart",
          "description": "Request Root Cause Analysis document for VM restart issues",
          "supportTopicId": "32628280",
          "commonSolutionArticleId": "1052989d-6417-4985-b4af-0ffdb63302b9",
          "symptomId": ""
        }
      ]
    },
    {
      "id": "Virtual_Disk_Management_Issues",
      "title": "Virtual Disk Management Issues",
      "description": "Troubleshoot issues with managing virtual disks in Azure",
      "category": "Management",
      "searchTags": "disk, attach, mount, storage, manage, add, subscription, data, detach, server, restore",
      "supportTopicId": "",
      "subProblems": [
        {
          "id": "Resizing_virtual_disks",
          "title": "Resizing virtual disks",
          "description": "Guidance on resizing virtual disks",
          "supportTopicId": "32632142",
          "commonSolutionArticleId": "6c90898f-7758-42e3-97bf-d85745fe6c08",
          "symptomId": ""
        },
        {
          "id": "Attaching_or_detaching_virtual_disks",
          "title": "Attaching or detaching virtual disks",
          "description": "Guidance on attaching or detaching a virtual disk to/from VMs",
          "supportTopicId": "32632139",
          "commonSolutionArticleId": "d43073c5-75dc-4c03-b04a-aa4c56e765a8",
          "symptomId": ""
        },
        {
          "id": "Creating_or_deleting_virtual_disks",
          "title": "Creating or deleting virtual disks",
          "description": "Guidance on deleting virtual disks",
          "supportTopicId": "32632140",
          "commonSolutionArticleId": "d43073c5-75dc-4c03-b04a-aa4c56e765a8",
          "symptomId": ""
        }
      ]
    },
    {
      "id": "Encryption_Issues",
      "title": "Encryption Issues",
      "description": "Troubleshoot encryption issues of Azure VM and/or disks",
      "category": "Management",
      "searchTags": "disk, encryption, encrypt, data, key, decrypt, drive, manage, bitlocker",
      "supportTopicId": "",
      "subProblems": [
        {
          "id": "Encrypt_VM_disk",
          "title": "Encrypt VM disk",
          "description": "Guidance on encrypting a VM disk",
          "supportTopicId": "32518038",
          "commonSolutionArticleId": "3b9c5dfb-2a76-453e-a9c7-c2f048634b46",
          "symptomId": ""
        },
        {
          "id": "Manage_encrypted_disks_keys_or_secrets_or_permissions",
          "title": "Manage encrypted disks, keys or secrets, or permissions",
          "description": "Guidance on managing encrypted disks, keys or secrets, or permissions",
          "supportTopicId": "32518039",
          "commonSolutionArticleId": "3b9c5dfb-2a76-453e-a9c7-c2f048634b46",
          "symptomId": ""
        },
        {
          "id": "Azure_Disk_Encryption_extension issue",
          "title": "Azure Disk Encryption (ADE) extension issue",
          "description": "Troubleshoot issues with Azure Disk Encryption extension",
          "supportTopicId": "32628258",
          "commonSolutionArticleId": "904eaea6-a9a3-454b-88c6-46fb04db2640",
          "symptomId": ""
        }
      ]
    },
    {
      "id": "VM_Extension_Issues",
      "title": "VM Extension Issues",
      "description": "Troubleshoot issues installing and/or executing Azure VM extensions",
      "category": "Deployment",
      "searchTags": "extension, agent, disk, encryption, backup, install, installation, encrypt, diagnostic, server, metric, script, provision, data",
      "supportTopicId": "",
      "subProblems": [
        {
          "id": "VM_Diagnostic_extension issue",
          "title": "VM Diagnostic (boot diagnostics) extension issue",
          "description": "Troubleshoot issues with VM Diagnostic extension",
          "supportTopicId": "32628283",
          "commonSolutionArticleId": "f0b4963f-5a47-420c-84de-c15b35d4dc50",
          "symptomId": ""
        },
        {
          "id": "Azure_Custom_Script_extension_issue",
          "title": "Azure Custom Script (CSE) extension issue",
          "description": "Troubleshoot issues with Azure Custom Script extension",
          "supportTopicId": "32628256",
          "commonSolutionArticleId": "a9463661-5253-4fbf-86a8-e4b379b1cf1c",
          "symptomId": ""
        },
        {
          "id": "Log_Analytics_extension_issue",
          "title": "Log Analytics (OMS) extension issue",
          "description": "Troubleshoot issues with Log Analytics extension",
          "supportTopicId": "32628273",
          "commonSolutionArticleId": "5cc8fa1d-ebd2-4b5e-b455-b2121c2663b5",
          "symptomId": ""
        },
        {
          "id": "Azure_Desired_State_Configuration_extension_issue",
          "title": "Azure Desired State Configuration (DSC) extension issue",
          "description": "Troubleshoot issues with Azure Desired State Configuration extension",
          "supportTopicId": "32628257",
          "commonSolutionArticleId": "f5523bca-7725-4d82-b461-6ae3962da477",
          "symptomId": ""
        },
        {
          "id": "Microsoft_Antimalware_extension_issue",
          "title": "Microsoft Antimalware (security) extension issue",
          "description": "Troubleshoot issues with Microsoft Antimalware extension",
          "supportTopicId": "32628276",
          "commonSolutionArticleId": "ed15f47e-da85-4b91-bce5-d03f6b3a6ade",
          "symptomId": ""
        },
        {
          "id": "Azure_Disk_Encryption_extension_issue",
          "title": "Azure Disk Encryption (ADE) extension issue",
          "description": "Troubleshoot issues with Azure Disk Encryption extension",
          "supportTopicId": "32628258",
          "commonSolutionArticleId": "904eaea6-a9a3-454b-88c6-46fb04db2640",
          "symptomId": ""
        },
        {
          "id": "VM_Snapshot_extension_issue",
          "title": "VM Snapshot (Azure Backup) extension issue",
          "description": "Troubleshoot issues with VM Snapshot extension",
          "supportTopicId": "32628288",
          "commonSolutionArticleId": "950a7bc9-306f-47b1-840f-8a1287f5ec3b",
          "symptomId": ""
        },
        {
          "id": "Extension_not_installing_correctly",
          "title": "Extension not installing correctly",
          "description": "Troubleshoot issues when VM extension is not installing correctly",
          "supportTopicId": "32628266",
          "commonSolutionArticleId": "cd2fec93-b941-40e5-ae9e-9461817e53de",
          "symptomId": ""
        },
        {
          "id": "Extension_not_executing_correctly",
          "title": "Extension not executing correctly",
          "description": "Troubleshoot issues when VM extension is not executing correctly",
          "supportTopicId": "32628267",
          "commonSolutionArticleId": "cd2fec93-b941-40e5-ae9e-9461817e53de",
          "symptomId": ""
        },
        {
          "id": "Update_Management_extension_issue",
          "title": "Update Management extension issue",
          "description": "Troubleshoot issues with Update Management extension",
          "supportTopicId": "32633803",
          "commonSolutionArticleId": "cd2fec93-b941-40e5-ae9e-9461817e53de",
          "symptomId": ""
        }
      ]
    },
  	{					   
      "id": "Troubleshoot_WindowsVirtualDeskTop",
      "title": "Troubleshoot Windows Virtual Desktop",
      "description": "Troubleshoot Windows Virtual Desktop issues",
      "category": "Windows Virtual Products",
      "searchTags": "WVD, Windows Virtual Desktop",
      "supportTopicId": "",
      "subProblems": [
			{
          "id": "VD_CommonIssues",
          "title": "Common Issues",
          "description": "Troubleshoot Common Issues",
          "supportTopicId": "32625539",
          "commonSolutionArticleId": "586ec56a-93f1-4c0c-86c0-63debae7b9f8",
          "symptomId": ""
        },
        {
          "id": "WVD_ARMTemplate",
          "title": "ARM template issues",
          "description": "Troubleshoot Azure Resource Manager template issues",
          "supportTopicId": "32727878",
          "commonSolutionArticleId": " Needed ",
          "symptomId": ""
        },
        {
          "id": "WVD_PowershellDSC issues",
          "title": "Desired State Configuration (DSC) issues",
          "description": "Troubleshoot Desired State Configuration (DSC) errors",
          "supportTopicId": "32727878",
          "commonSolutionArticleId": " Needed ",
          "symptomId": ""
        },
        {
          "id": "WVD_FXLogicIssues",
          "title": "FXLogix issues",
          "description": "Troubleshoot FXLogix issues",
          "supportTopicId": "32681783",
          "commonSolutionArticleId": "803975e4-6094-4086-95ff-2896a7e7902f",
          "symptomId": ""
        },
        {
          "id": "WVD_SpringUpdate",
          "title": "Spring Update Issues",
          "description": "Troubleshoot Spring Update Issues",
          "supportTopicId": "32740695",
          "commonSolutionArticleId": "2a0f5b97-41f3-44d6-8a1f-f25ad89822fe",
          "symptomId": ""
        },
        {
          "id": "WVD_Tenant",
          "title": "Tenant Issues",
          "description": "Issues creating Windows Virtual Desktop tenant",
          "supportTopicId": "32727880",
          "commonSolutionArticleId": "8f53a07f-1c5d-4b08-9510-96b41e6d065b",
          "symptomId": ""
        },
        {
          "id": "WVD_DomainConfig",
          "title": "Domain Configuration",
          "description": "Issues configuring your domain",
          "supportTopicId": "32727876",
          "commonSolutionArticleId": "53fb2b60-cfd0-4e5a-b9fb-f8bf83acc01d",
          "symptomId": ""
        },
        {
          "id": "WVD_DeviceRedirection",
          "title": "Device Redirection",
          "description": "Issues configuring device redirection",
          "supportTopicId": "32727874",
          "commonSolutionArticleId": "032cf025-2f52-4420-b161-bce71302f41b",
          "symptomId": ""
        },
        {
          "id": "WVD_HostPoolSessionHost",
          "title": "HostPool/SessionHost",
          "description": "Creating a host pool or session host",
          "supportTopicId": "32727879",
          "commonSolutionArticleId": "1b9984b1-6b6c-4f67-9415-a597c3de8112",
          "symptomId": ""
        }
      ]
    },
    {
      "id": "Backup_and_Restore",
      "title": "Backup and Restore",
      "description": "Troubleshoot issues creating a backup or restoring from backup",
      "category": "Management",
      "searchTags": "backup, server, restore, snapshot, configure, vault, data, disk, sql, agent, recovery, server, ssd, on premise, download, vhd, capture, image, clone, restore",
      "supportTopicId": "",
      "subProblems": [
        {
          "id": "Troubleshoot_backup_issues",
          "title": "Troubleshoot backup issues",
          "description": "Troubleshoot issues when backing up a single VM, multiple VMs, or VM disks",
          "supportTopicId": "32565494",
          "commonSolutionArticleId": "15c87a05-eb46-4369-bea4-8d2b3af57dce",
          "symptomId": ""
        },
        {
          "id": "Restore_VM_from_Snapshot",
          "title": "Restore VM from Snapshot",
          "description": "Troubleshoot issues when restoring a VM from Snapshot",
          "supportTopicId": "32632143",
          "commonSolutionArticleId": "139e0b4c-3609-4472-930e-e61306f5818e",
          "symptomId": ""
        },
        {
          "id": "VM_Snapshot_extension_issue",
          "title": "VM Snapshot (Azure Backup) extension issue",
          "description": "Troubleshoot issues with VM Snapshot extension",
          "supportTopicId": "32628288",
          "commonSolutionArticleId": "950a7bc9-306f-47b1-840f-8a1287f5ec3b",
          "symptomId": ""
        }
      ]
    }
  ],
  "troubleshootingTools": [
    {
      "id": "Redeploy_virtual_machine_tool",
      "title": "Redeploy virtual machine",
      "description": "Migrate and redeploy this virtual machine to a different Azure host",
      "category": "Deployment",
      "searchTags": "deploy, deployment, host, connectivity",
      "type": "tool",
      "bladeLink": {
        "extensionName": "Microsoft_Azure_Compute",
        "bladeName": "VirtualMachineRedeployViewModel",
        "parameters": [
          {
            "name": "id",
            "value": "$resourceId"
          }
        ]
      }
    },
    {
      "id": "Reset_RDP_account_configuration_tool",
      "title": "Reset RDP account and configuration for VM",
      "description": "Resets the built-in administrator account and the Remote Desktop service configuration",      
      "category": "Deployment",
      "searchTags": "password, rdp, user, credentials, remote desktop, admin, privilege",
      "type": "tool",
      "bladeLink": {
        "extensionName": "Microsoft_Azure_Compute",
        "bladeName": "VirtualMachinePasswordReset",
        "parameters": [
          {
            "name": "id",
            "value": "$resourceId"
          }
        ]
      }
    },
    {
      "id": "Serial_Console_tool",
      "title": "Serial Console",
      "description": "Log on to virtual machine's serial console",      
      "category": "Connectivity",
      "searchTags": "serial console, connect VM, console access",
      "type": "tool",
      "bladeLink": {
        "extensionName": "Microsoft_Azure_Compute",
        "bladeName": "VmSerialConsoleValidationBlade",
        "parameters": [
          {
            "name": "id",
            "value": "$resourceId"
          },
          {
            "name": "resourceId",
            "value": "$resourceId"
          }
        ]
      }
    },
    {
      "id": "Boot_Diagnostics_tool",
      "title": "Boot Diagnostics",
      "description": "View the serial console output and a screenshot of this virtual machine to help diagnose startup issues",      
      "category": "Connectivity",
      "searchTags": "screenshot, logs, console output, boot, diagnostics, startup",
      "type": "tool",
      "bladeLink": {
        "extensionName": "Microsoft_Azure_Compute",
        "bladeName": "SerialConsoleLogBladeViewModel",
        "parameters": [
          {
            "name": "id",
            "value": "$resourceId"
          },
	  {
            "name": "resourceId",
            "value": "$resourceId"
          }
        ]
      }
    },
    {
      "id": "Verify_IP_flow_tool",
      "title": "Verify IP flow",
      "description": "Use IP flow verify to confirm if a rule in a Network Security Group or user defined route is blocking traffic to or from a virtual machine",      
      "category": "Connectivity",
      "searchTags": "NSG, network troubleshoot, network security group, network, networking",
      "type": "tool",
      "bladeLink": {
        "extensionName": "microsoft_azure_network",
        "bladeName": "VerifyIPFlowBlade",
        "parameters": [
          {
            "name": "id",
            "value": "$resourceId"
          }
        ]
      }
    },
    {
      "id": "Virtual_Machine_Health_tool",
      "title": "Virtual Machine Health",
      "description": "Use Azure Resource health to diagnose any issues with the resource. It monitors and indicates any availability issues.",      
      "category": "Management",
      "searchTags": "resource health, availability, restarts, VM restart, Health",
      "type": "tool",
      "bladeLink": {
        "extensionName": "Microsoft_Azure_Health",
        "bladeName": "ResourceHealthDetailBlade",
        "parameters": [
          {
            "name": "resourceId",
            "value": "$resourceId"
          }
        ]
      }
    },
    {
      "id": "Azure_Service_Health_tool",
      "title": "Azure Service Health",
      "description": "Use the Azure Service Health blade to see current service issues that may be affecting your resources",      
      "category": "Management",
      "searchTags": "outage, Azure issues, production, platform impact",
      "type": "tool",
      "bladeLink": {
        "extensionName": "Microsoft_Azure_Health",
        "bladeName": "ServiceIssuesBlade",
        "parameters": [
          {
            "name": "id",
            "value": "$resourceId"
          }
        ]
      }
    },
    {
      "id": "Audit_and_Activity_Log_tool",
      "title": "Audit and Activity Log",
      "description": "View Activity Logs to look at recent history of changes on this virtual machine",      
      "category": "Management",
      "searchTags": "audit, history, what happened, who changed, logs, recent changes, updates, events",
      "type": "tool",
      "bladeLink": {
        "extensionName": "Microsoft_Azure_Monitoring",
        "bladeName": "AzureDiagnosticsBladeWithParameter",
        "parameters": [
          {
            "name": "id",
            "value": "$resourceId"
          }
        ]
      }
    },
    {
      "id": "Performance_diagnostics_tool",
      "title": "Performance diagnostics",
      "description": "Troubleshoot performance issues on the virtual machine",      
      "category": "Performance",
      "searchTags": "VM, performance, high, low, CPU, memory, disk, throughput, throttling",
      "type": "tool",
      "bladeLink": {
        "extensionName": "Microsoft_Azure_Compute",
        "bladeName": "PerformanceDiagnosticsBlade",
        "parameters": [
          {
            "name": "id",
            "value": "$resourceId"
          },
	  {
            "name": "resourceId",
            "value": "$resourceId"
          }
        ]
      }
    },
    {
      "id": "Troubleshoot_network_connectivity_tool",
      "title": "Troubleshoot network connectivity",
      "description": "Check and test direct TCP connections from the VM to another VM, fully qualified domain name (FQDN), URI, or an IPv4 address",
      "category": "Connectivity",
      "searchTags": "test traffic, troubleshoot connectivity, unable to connect, network issues, unreachable",
      "type": "tool",
      "bladeLink": {
        "extensionName": "Microsoft_Azure_Network",
        "bladeName": "NetworkWatcherConnectivityBlade",
        "parameters": [
          {
            "name": "id",
            "value": "$resourceId"
          }
        ]
      }
    },
    {
      "id": "Virtual_Machine_metrics_tool",
      "title": "Virtual Machine metrics",
      "description": "View charts and metrics and counters data for the virtual machine",
      "category": "Management",
      "searchTags": "performance, metrics",
      "type": "tool",
      "bladeLink": {
        "extensionName": "Microsoft_Azure_Monitoring",
        "bladeName": "MetricsBladeV3",
        "parameters": [
          {
            "name": "id",
            "value": "$resourceId"
          }
        ]
      }
    },
    {
      "id": "Analyze_Recent_Changes_tool",
      "title": "Analyze recent changes",
      "description": "Use the Change Analysis service to see any changes made to this virtual machine and its related resources",
      "category": "Management",
      "searchTags": "audit, history, change",
      "type": "tool",
      "bladeLink": {
        "extensionName": "Microsoft_Azure_ChangeAnalysis",
        "bladeName": "ResourceChangesBlade",
        "parameters": [
          {
            "name": "resourceId",
            "value": "$resourceId"
          },
          {
            "name": "deepLinkOrigin",
            "value": "d&sp"
          }
        ]
      }
    }
  ]
}
---
