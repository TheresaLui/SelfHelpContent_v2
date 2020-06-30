<properties
pageTitle="Top common problems for compute"
description="Menu based workflow document for top compute problems"        
service="microsoft.compute"
resource="virtualmachines"
authors="gansmore,summertgu"
ms.author="ganesh.more,tiag"
displayOrder=""
articleId="0f103d3a-dc19-45af-b25d-de8338e002ce"
selfHelpType="diagnoseandsolve"
resourceTags="linux, ubuntu, redhat, suse"
productPesIds="15571"
cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines"
/>
# Diagnose and solve v2 test article for linux
---
{
  "$schema": "SelfHelpContent",
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
        "commonSolutionArticleId": "64d6c5db-c7b8-4895-bfcc-010ad6155ba4",
        "symptomId": ""
      },
      {
        "id": "Troubleshoot_network_security_group",
        "title": "Troubleshoot network security group (NSG)",
        "description": "Troubleshoot connectivity issues due to network security group rules",
        "supportTopicId": "32615530",
        "commonSolutionArticleId": "59a3aab3-768c-406c-a167-7f7dc1d481e3",
        "symptomId": ""
      },
      {
        "id": "Troubleshoot_VM_firewall",
        "title": "Troubleshoot VM firewall",
        "description": "Troubleshoot connectivity issues due to firewall rules",
        "supportTopicId": "32615534",
        "commonSolutionArticleId": "9300d912-0a92-4150-b9e2-e7c2461f54a9",
        "symptomId": ""
      },
      {
        "id": "Public_IP_issue",
        "title": "Public IP issue",
        "description": "Troubleshoot connectivity issues due to Public IP issues",
        "supportTopicId": "32615527",
        "commonSolutionArticleId": "0b945377-40b3-4d60-90ef-5e37b98ad0af",
        "symptomId": ""
      },
      {
        "id": "Serial_console_access",
        "title": "Serial console access",
        "description": "Understand how to use serial console to troubleshoot connectivity issues",
        "supportTopicId": "32615528",
        "commonSolutionArticleId": "509a4ecf-4efc-4ccb-b0bd-262bdc456b8f",
        "symptomId": ""
      },
      {
        "id": "Cannot_SSH",
        "title": "Cannot SSH",
        "description": "Troubleshoot connectivity issues to an Azure virtual machine",
        "supportTopicId": "32615526",
        "commonSolutionArticleId": "d160cd1f-4883-415c-ad18-8e2c146743d7",
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
          "commonSolutionArticleId": "e32c32c4-edf2-470f-a731-7f4fe2cff95d",
          "symptomId": ""
        },
        {
          "id": "CPU_usage_high",
          "title": "CPU usage is higher than expected",
          "description": "Troubleshoot performance issues when CPU usage is higher than expected",
          "supportTopicId": "32628261",
          "commonSolutionArticleId": "d0fa4014-1b31-4dea-beaa-0e7d1ef6d466",
          "symptomId": ""
        },
        {
          "id": "Memory_usage_high",
          "title": "Memory usage is higher than expected",
          "description": "Troubleshoot performance issues when memory usage is higher than expected",
          "supportTopicId": "32628275",
          "commonSolutionArticleId": "d2aaff89-b196-425a-99ed-15656d09fbd1",
          "symptomId": ""
        },
        {
          "id": "GPU_processing_slow",
          "title": "GPU processing is slower than expected",
          "description": "Troubleshoot performance issues when GPU processing is slower than expected",
          "supportTopicId": "32628268",
          "commonSolutionArticleId": "2f101132-9899-437e-a74f-f5dd404fd8f9",
          "symptomId": ""
        },
        {
          "id": "Unable_to_resize_my_VM",
          "title": "Unable to resize my VM",
          "description": "Unable to resize Azure VMs",
          "supportTopicId": "32690776",
          "commonSolutionArticleId": "d2152bb1-ed42-4865-bc62-9f391603ea92",
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
          "commonSolutionArticleId": "4bdc4ff0-cbe2-4886-a8f7-ef6a227b52f9",
          "symptomId": ""
        },
        {
          "id": "Provisioning_or_deployment_timeout_error",
          "title": "Provisioning or deployment timeout error",
          "description": "Troubleshoot provisioning or deployment timeout errors when creating a new VM in Azure",
          "supportTopicId": "32628279",
          "commonSolutionArticleId": "6824513e-6cd0-4641-9c47-1abc6533f4a6",
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
          "commonSolutionArticleId": "226e1a7a-d31d-4501-b094-7033313279b6",
          "symptomId": ""
        },
        {
          "id": "Marketplace_image_deployment_failure",
          "title": "Marketplace image deployment failure",
          "description": "Troubleshoot issues when deploying a marketplace image",
          "supportTopicId": "32628274",
          "commonSolutionArticleId": "85e53d67-cc97-4a46-ba63-20c752e97af1",
          "symptomId": ""
        }
      ]
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
          "commonSolutionArticleId": "39af50e8-5008-40f4-809f-6dc6e1e71f93",
          "symptomId": ""
        },
        {
          "id": "Prepare_an_image",
          "title": "Prepare an image",
          "description": "Guidance on capturing a VM to image in Azure",
          "supportTopicId": "32628272",
          "commonSolutionArticleId": "f4150867-4326-4684-bcae-b68b323026cc",
          "symptomId": ""
        },
        {
          "id": "Choosing_Region_or_VM_size",
          "title": "Choosing Region or VM size",
          "description": "Guidance on creating a new VM in an unavailable size or region, or when finding suitable SKU for deployment",
          "supportTopicId": "32628263",
          "commonSolutionArticleId": "9c65e013-d2bf-4376-87cd-b34554d71bf7",
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
      "commonSolutionArticleId": "28c55293-b977-4d19-b98c-338f450a6aa4",
      "symptomId": ""
    },
    {
      "id": "VM_is_not_booting",
      "title": "VM is not booting",
      "description": "Troubleshoot common boot errors for non-bootable VMs",
      "category": "Connectivity",
      "searchTags": "stuck, boot, start, fail, server, restart, reboot, update, disk, load, storage, encryption",
      "supportTopicId": "32628284",
      "commonSolutionArticleId": "0c333e4e-a865-4822-84b4-0c8eba727ffe",
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
    "id": "Help_with_VM_Sizing",
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
        "commonSolutionArticleId": "b9eb1036-325b-40aa-b5fe-d2a55fd25848",
        "symptomId": ""
      },
      {
        "id": "Unable_to_resize_my_VM",
        "title": "Unable to resize my VM",
        "description": "Unable to resize Azure VMs",
        "supportTopicId": "32632142",
        "commonSolutionArticleId": "b9eb1036-325b-40aa-b5fe-d2a55fd25848",
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
          "commonSolutionArticleId": "845b0f97-0026-43f2-aaea-daf3cea70cb8",
          "symptomId": ""
        },
        {
          "id": "Disk_related_error",        
          "title": "Disk related error",
          "description": "Troubleshoot disk related errors when starting a VM in Azure",
          "supportTopicId": "32628265",
          "commonSolutionArticleId": "f4b36484-b9e9-4024-8ca1-3f56024eea91",
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
          "commonSolutionArticleId": "d4d90945-3e9c-4139-aa2e-13824a736385",
          "symptomId": ""
        },
        {
          "id": "Start_or_stop_operation_failed",
          "title": "Start or stop operation failed",
          "description": "Troubleshoot failures when starting or stopping a VM in Azure",
          "supportTopicId": "32628282",
          "commonSolutionArticleId": "aa0bafee-2385-4cb8-8352-dd65f180361a",
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
          "commonSolutionArticleId": "b66f3036-bc84-4466-8934-8b630c022deb",
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
          "commonSolutionArticleId": "aea5b2c8-7393-49a1-b9eb-e32910bc0eaf",
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
          "commonSolutionArticleId": "b9eb1036-325b-40aa-b5fe-d2a55fd25848",
          "symptomId": ""
        },
        {
          "id": "Attaching_or_detaching_virtual_disks",
          "title": "Attaching or detaching virtual disks",
          "description": "Guidance on attaching or detaching a virtual disk to/from VMs",
          "supportTopicId": "32632139",
          "commonSolutionArticleId": "3cef1f67-f2f8-4a0e-887b-6a9aa09fcf27",
          "symptomId": ""
        },
        {
          "id": "Creating_or_deleting_virtual_disks",
          "title": "Creating or deleting virtual disks",
          "description": "Guidance on deleting virtual disks",
          "supportTopicId": "32632140",
          "commonSolutionArticleId": "3cef1f67-f2f8-4a0e-887b-6a9aa09fcf27",
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
          "commonSolutionArticleId": "8b8135ac-b1d3-4f51-a983-0d03ccf4320f",
          "symptomId": ""
        },
        {
          "id": "Manage_encrypted_disks_keys_or_secrets_or_permissions",
          "title": "Manage encrypted disks, keys or secrets, or permissions",
          "description": "Guidance on managing encrypted disks, keys or secrets, or permissions",
          "supportTopicId": "32518039",
          "commonSolutionArticleId": "8b8135ac-b1d3-4f51-a983-0d03ccf4320f",
          "symptomId": ""
        },
        {
          "id": "Azure_Disk_Encryption_extension issue",
          "title": "Azure Disk Encryption (ADE) extension issue",
          "description": "Troubleshoot issues with Azure Disk Encryption extension",
          "supportTopicId": "32628258",
          "commonSolutionArticleId": "673be084-45c4-4cf0-a67a-2d4f8231b8f3",
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
          "commonSolutionArticleId": "0f978043-20db-48ba-a5f7-e75b32083c75",
          "symptomId": ""
        },
        {
          "id": "Azure_Custom_Script_extension_issue",
          "title": "Azure Custom Script (CSE) extension issue",
          "description": "Troubleshoot issues with Azure Custom Script extension",
          "supportTopicId": "32628256",
          "commonSolutionArticleId": "0f978043-20db-48ba-a5f7-e75b32083c75",
          "symptomId": ""
        },
        {
          "id": "Log_Analytics_extension_issue",
          "title": "Log Analytics (OMS) extension issue",
          "description": "Troubleshoot issues with Log Analytics extension",
          "supportTopicId": "32628273",
          "commonSolutionArticleId": "4c3f9765-562b-492b-9945-ac75d872add3",
          "symptomId": ""
        },
        {
          "id": "Azure_Desired_State_Configuration_extension_issue",
          "title": "Azure Desired State Configuration (DSC) extension issue",
          "description": "Troubleshoot issues with Azure Desired State Configuration extension",
          "supportTopicId": "32628257",
          "commonSolutionArticleId": "b368f184-63a5-4bfd-be56-a58b91b4376c",
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
          "commonSolutionArticleId": "673be084-45c4-4cf0-a67a-2d4f8231b8f3",
          "symptomId": ""
        },
        {
          "id": "VM_Snapshot_extension_issue",
          "title": "VM Snapshot (Azure Backup) extension issue",
          "description": "Troubleshoot issues with VM Snapshot extension",
          "supportTopicId": "32628288",
          "commonSolutionArticleId": "c5847b30-7196-44dd-9861-40d19c77298c",
          "symptomId": ""
        },
        {
          "id": "Extension_not_installing_correctly",
          "title": "Extension not installing correctly",
          "description": "Troubleshoot issues when VM extension is not installing correctly",
          "supportTopicId": "32628266",
          "commonSolutionArticleId": "79c0e8f0-6de3-441b-a6a1-ec0be01155f8",
          "symptomId": ""
        },
        {
          "id": "Extension_not_executing_correctly",
          "title": "Extension not executing correctly",
          "description": "Troubleshoot issues when VM extension is not executing correctly",
          "supportTopicId": "32628267",
          "commonSolutionArticleId": "79c0e8f0-6de3-441b-a6a1-ec0be01155f8",
          "symptomId": ""
        },
        {
          "id": "Update_Management_extension_issue",
          "title": "Update Management extension issue",
          "description": "Troubleshoot issues with Update Management extension",
          "supportTopicId": "32633803",
          "commonSolutionArticleId": "d530b6fe-3096-40c1-9ef0-2bc37364bee5",
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
          "commonSolutionArticleId": "3f754469-b316-40d3-9888-c36f5cdf51b5",
          "symptomId": ""
        },
        {
          "id": "VM_Snapshot_extension_issue",
          "title": "VM Snapshot (Azure Backup) extension issue",
          "description": "Troubleshoot issues with VM Snapshot extension",
          "supportTopicId": "32628288",
          "commonSolutionArticleId": "c5847b30-7196-44dd-9861-40d19c77298c",
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
      "id": "Reset_SSH_public_key_or_password_tool",
      "title": "Reset SSH public key or password",
      "description": "Reset the SSH public key or password of the an account with sudo privileges",
      "category": "Deployment",
      "searchTags": "password, ssh, user, credentials, sudo privilege, admin, root",
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
