<properties
  pagetitle="Vulnerability Assessment - Built-In (Powered by Qualys) self help guide&#xD;"
  ms.author="kawilson,elsagie"
  selfhelptype="Generic"
  supporttopicids="32749421"
  resourcetags=""
  productpesids="15947"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="6bc4e686-7ac5-4850-80dc-ac802cf2bee5"
  ownershipid="Azure_Security_Security_Center" />
# Vulnerability Assessment - Built-In (Powered by Qualys) self help guide

### My machine is not in the recommended list for enabling a vulnerability assessment solution
1. Make sure the [vulnerability assessment policy](https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2fproviders%2fMicrosoft.Authorization%2fpolicyDefinitions%2f501541f7-f7e7-4cd6-868c-4190fdad3ac9) is assigned to your subscription.
2. Check to see if your machine is in the Not Applicable tab. If it is, this could be why the machine is in that state:
   a. It might be an unsupported resource type. See supported resources and operating systems in the [documentation](https://docs.microsoft.com/azure/security-center/deploy-vulnerability-assessment-vm)
   b. If you see a message saying that the extension might be corrupted, try to remove or unlink the vulnerability assessment extension for this machine. Then wait for it to be recommended for deployment and try to deploy it again.

### My machine fails for successfully deploy the vulnerability scanner
1. Check the [documentation](https://docs.microsoft.com/azure/security-center/deploy-vulnerability-assessment-vm#deploy-the-integrated-scanner-to-your-azure-and-hybrid-machines) to see you are running a supported operating system 
2. Make sure your machine is turned on. If this is an Azure Arc machine, make sure it is in the Connected state and not Offline.
3. Validate that you have Write permissions for the VM or Arc Machine.
4. Make sure your machine has internet access to the vulnerability scanning platform. If you are using the Qualys scanner, see the network requirements in the [these FAQs](https://docs.microsoft.com/azure/security-center/deploy-vulnerability-assessment-vm#what-prerequisites-and-permissions-are-required-to-install-the-qualys-extension).
5. Check if you have sufficient disk space: at least 512 MB RAM and 200 MB disk space.

### My machine doesn’t have vulnerability findings in the "Remediate vulnerabilities in your virtual machines" assessment
1. Make sure your scanner is successfully deployed by making sure your machine has a Healthy status on the scanner provisioning assessment, "A vulnerability assessment solution should be enabled on your virtual machines." If it doesn’t, successfully deploy a vulnerability scanner on your machine.
2. Check the machine status on the findings assessment, **"Remediate vulnerabilities in your virtual machines"**.
   a. If it has Healthy status, no vulnerabilities were found on that machine.
   b. If it has Not Applicable status, check the reason column to get more details.  

A common reason is "Findings have not been received yet for the VM", which is typical for new agent deployments. It may take up to 24 hours for the scanner vendor to register the new agent and complete a full first scan. However, after first the first scan appears, subsequent scans are typically reflected in ASC minutes after being completed by the machine.

### I tried to manually install the extension via Compute API and failed
Installing the integrated vulnerability assessment scanners integrated with ASC should be done through ASC API.
-	If you are using the built-in vulnerability assessment scanner, see [this blog post](https://techcommunity.microsoft.com/t5/azure-security-center/built-in-vulnerability-assessment-for-vms-in-azure-security/ba-p/1577947) for all deployment as scale options.  

### My machine keeps appearing under N/A resources with the reason "extension might be corrupted" even though I removed and reinstalled it.
Make sure that the extension was not re-installed manually via Compute extensions API, since installing VA can only be established via ASC. 
-	If you are using the built-in vulnerability assessment scanner, see [this blog post](https://techcommunity.microsoft.com/t5/azure-security-center/built-in-vulnerability-assessment-for-vms-in-azure-security/ba-p/1577947) for all deployment as scale options.   

### I resolved my machine’s vulnerability findings, but I can still see them in ASC
It may take a few hours for the next vulnerability scan cycle to run and reflect the changes in ASC.

### My security solution (or VM) shows "Not Reported" health status
This means ASC did not receive a health status from the scanner vendor. If the issue persists, open a support ticket with your vulnerability scanner vendor.

### Linking a VM to my solution fails and the extension is not installed
If you have more than one security solution configured, make sure your VM is not already linked to another one.

### Creating a new solution fails 
Make sure the license you entered is not already used for a different solution in the same subscription.

## **Recommended Documents**

- [Scan your VMs with a BYOL VA solution](https://docs.microsoft.com/azure/security-center/deploy-vulnerability-assessment-byol-vm)
- [Review and remediate vulnerabilities](https://docs.microsoft.com/azure/security-center/remediate-vulnerability-findings-vm)
- [Disable specific vulnerability findings](https://docs.microsoft.com/azure/security-center/remediate-vulnerability-findings-vm#disable-specific-findings-preview)

### Troubleshooting

- [ASC Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

### FAQ

- [ASC FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)
