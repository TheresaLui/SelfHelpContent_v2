<properties
    pageTitle="Missing Scan Data Common Solutions"
    description="Missing Scan Data Common Solutions"
    service=""
    resource=""
    authors="TobyTu"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32636883"
    resourceTags=""
    productPesIds="15947"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="a15f057d-8uj6-4b00-a98a-dfaf0843dc2f"
	ownershipId="Azure_Security_Security_Center"
/>

# Missing Scan Data Common Solutions

This message appears when there is no scan data for a VM. It can take some time (less than an hour) for scan data to populate after Data Collection is enabled in Azure Security Center. After the initial population of scan data, you may receive this message because there is no scan data at all or there is no recent scan data. Scans do not populate for a VM in a stopped state.

## **Recommended Steps**

### Step 1 : Troubleshooting Guide for Resolving Missing Scan Data for Anti-malware

- Azure Security Center support Windows Defender Anti-Malware and third party vendors  based on [this list](https://docs.microsoft.com/azure/security-center/security-center-os-coverage#supported-endpoint-protection-solutions)
- Anti-malware assessment supports currently only on Windows VM
- Refresh Data for Anti-Malware status data is updated within 8 hours
- Check if the agent of the VM is healthy and reported heartbeat to the workspace, VM with problematic agent state will report missing scan data on the Anti-malware
- Run the below query against log analytics workspace to find out the Anti-malware status that we collect from the protected VM:

    1. Open log analytics
    2. Select the relevant workspace that the VM connect to it
    3. Press "logs" in the left navigation
    4. Run this query (replace the VM name)

       ```/
       ProtectionStatus
       | where TimeGenerated > ago(1d)
       | where Computer contains "MyVMName"
       ```

    5. Expend for the results, and examine these fields
       |   |   |
       | - | - |
       |  Type of Protection | Name of the anti-malware that installed on the VM |
       | Protection Status Rank | ID that represents the status of the Anti-malware |
       |Threat Status Rank| ID that represents the status of the Anti-malware thread protection|

       For most of the anti-malware vendors the current status for this two ID's is 150. Here is the full list for the status:

       ```/
       Threat Status Rank
       Active  550
       Unknown  470
       Remediated  370
       Quarantined  350
       Blocked  330
       Allowed  250
       No threats detected  150
       -
       Protection Status Rank
       Threat Detected  550
       Unknown  470
       Not Reporting  450
       Action Required  350
       No real time protection  270
       Signatures out of date  250
       Real time protection 150
       ```

### Step 2 : Troubleshooting Guide for Resolving Missing Scan Data for Windows Update

- Azure Security Center assists your security and critical update for Linux and windows VM and on-premises servers
- Refresh time for System updates data is updated within 24 hours
- Check if the agent of the VM is healthy and reported heartbeat to the workspace, VM with problematic agent state will report missing scan data on the windows update
- Run the below query against log analytics workspace to find out the missing updates status that we collect from the protected VM:

   1. Open log analytics
   2. Select the relevant workspace that the VM connect to it
   3. Press "logs" in the left navigation
   4. Run this query (just replace the VM name)

      ```/
      Update
      | where TimeGenerated > ago(1d)
      | where Computer contains "YourVMname"
      | where Classification == "Security Updates" or Classification == "Critical Updates" and UpdateState =~ "Needed"
      ```

The results will show us the missing update based on Azure Security Center classification. If you are seeing Incompatibility check windows\Linux update logs for the given VM.

### Step 3 : Troubleshooting Guide for Resolving Missing Scan Data for Security Configuration

Azure Security Center monitors security configurations by applying a set of [over 150 recommended rules](https://gallery.technet.microsoft.com/Azure-Security-Center-a789e335) for hardening the OS.

- Check if the agent of the VM is healthy and reported heartbeat to the workspace, VM with problematic agent state will report missing scan data on the security configuration
- Operating system security configurations data is updated within 48 hours

   ```/
   SecurityBaselineSummary
   | where TimeGenerated > ago(1d)
   | where Computer contains "type1000000"
   ```

- Run the below query against log analytics workspace to find out the missing updates status that we collect from the protected VM:

   1. Open log analytics
   2. Select the relevant workspace that the VM connect to it
   3. Press "logs" in the left navigation
   4. Run this query (replace the VM name)

      ```/
      SecurityBaselineSummary
      | where TimeGenerated > ago(2d)
      | where Computer contains "type1000000"
      ```

## **Recommended Documents**

- [Platforms and features supported by Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-os-coverage)
- [Exploring Microsoft Antimalware Alert in Azure Security Center](https://blogs.technet.microsoft.com/yuridiogenes/2018/08/20/exploring-microsoft-antimalware-alert-in-azure-security-center/)

**Troubleshooting**

- [Azure Security Center Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

**FAQ**

- [Azure Security Center FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)