<properties
  pagetitle="Vulnerability Assessment - Solutions (BYOL) self help guide&#xD;"
  ms.author="amaviram,agolden"
  selfhelptype="Generic"
  supporttopicids="32749421"
  resourcetags=""
  productpesids="15947"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="6bc4e686-7ac5-4850-80dc-ac802cf2bee5"
  ownershipid="Azure_Security_Security_Center" />
# Vulnerability Assessment - Solutions (BYOL) self help guide

### **My machine is not in the recommended list for enabling a vulnerability assessment solution**
- Make sure the [vulnerability assessment policy](https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2fproviders%2fMicrosoft.Authorization%2fpolicyDefinitions%2f501541f7-f7e7-4cd6-868c-4190fdad3ac9) is assigned to your subscription.
- Check to see if your machine is in the **Not Applicable** tab. If it is, the **Reason** could explain why the machine is at that state. Make sure that your machine is a supported resource type. See [supported resources and operating systems](https://docs.microsoft.com/azure/security-center/deploy-vulnerability-assessment-vm). If you see a message saying that the extension might be corrupted, try to remove or unlink the vulnerability assessment extension for this machine. Wait for it to be recommended for deployment and try to deploy it again.


### My machine fails for successfully deploying the vulnerability scanner
- Check the [documentation](https://docs.microsoft.com/azure/security-center/deploy-vulnerability-assessment-vm#deploy-the-integrated-scanner-to-your-azure-and-hybrid-machines) to see if you are running a supported operating system. 
- If you cannot enable the vulnerability assessment solution on your VM, see [VM agent Windows](https://docs.microsoft.com/azure/virtual-machines/extensions/agent-windows) or [VM agent Linux](https://docs.microsoft.com/azure/virtual-machines/extensions/agent-linux)
- Make sure your machine is turned on.
- Validate that you have Write permissions for the VM or Arc Machine.
- Make sure that your machine has internet access to the vulnerability scanning platform. If you are using the Qualys scanner, see the [network requirements in the FAQ](https://docs.microsoft.com/azure/security-center/deploy-vulnerability-assessment-vm#what-prerequisites-and-permissions-are-required-to-install-the-qualys-extension).
- Check that you have sufficient disk space (at least 512MB RAM and 200MB disk space).


### My machine doesn’t have vulnerability findings in the **Remediate vulnerabilities in your virtual machines** assessment
- Make sure that your scanner is successfully deployed. Check that your machine has a Healthy status on the following scanner provisioning assessment, "A vulnerability assessment solution should be enabled on your virtual machines". If it doesn’t have a Healthy status, deploy a vulnerability scanner on that machine.
- Check the machine status on the findings assessment, "Remediate vulnerabilities in your virtual machines."
    - If it has a Healthy status, no vulnerabilities were found on that machine.
    - If it has Not Applicable status, check the reason column to get more details.  
      A common reason is that "Findings have not been received yet for the VM", which is typical for new agent deployments. It may take up to 24 hours for the scanner vendor to register the new agent and complete a full first scan. However, after the first scan is shown, subsequent scans are typically reflected in ASC after a few hours.

### I tried to manually install the extension via Compute API and failed

Installing the integrated vulnerability assessment scanners integrated with ASC should be done through ASC API.
-	If you are using the built-in vulnerability assessment scanner, see [this blog post for all deployment as scale options](https://techcommunity.microsoft.com/t5/azure-security-center/built-in-vulnerability-assessment-for-vms-in-azure-security/ba-p/1577947)  

### My machine keeps appearing under N/A resources with the reason "extension might be corrupted" even though I removed and reinstalled it

Make sure that the extension was not reinstalled manually via the compute extensions API. Installing VA can only be established via ASC. 
- If you are using the built-in vulnerability assessment scanner, see [this blog post for all deployment as scale options](https://techcommunity.microsoft.com/t5/azure-security-center/built-in-vulnerability-assessment-for-vms-in-azure-security/ba-p/1577947).

### I resolved my machine’s vulnerability findings, but I can still see them in ASC

It may take a few hours for the next vulnerability scan cycle to run and reflect the changes in ASC. If the issue persists, open a support ticket with your vulnerability scanner vendor.

### My security solution (or VM) shows **Not Reported** health status

This means that ASC did not receive a health status from the scanner vendor. If the issue persists, open a support ticket with your vulnerability scanner vendor.

### Linking a VM to my solution fails and the extension is not installed

If you have more than one security solution configured, make sure your VM is not already linked to another one.

### **Creating a new solution fails** 

Make sure that the license you entered is not already used for a different solution in the same subscription.

### I can't find my VMs in the list displayed by "Link VM" button

Linking VMs to Security Solutions in ASC can only be for eligible VMs from the same subscription of the solution. If that's the case, and the VM is still not in that list, go to the recommendation, "A vulnerability assessment solution should be enabled on your virtual machines", and look for the VM in the **Not Applicable** tab to find the reason it is there.

## **Recommended Documents**

- [Scan your VMs with a BYOL VA solution](https://docs.microsoft.com/azure/security-center/deploy-vulnerability-assessment-byol-vm)
- [Review and remediate vulnerabilities](https://docs.microsoft.com/azure/security-center/remediate-vulnerability-findings-vm)
- [Disable specific vulnerability findings](https://docs.microsoft.com/azure/security-center/remediate-vulnerability-findings-vm#disable-specific-findings-preview)

### Troubleshooting

- [ASC Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

### FAQ

- [ASC FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)
