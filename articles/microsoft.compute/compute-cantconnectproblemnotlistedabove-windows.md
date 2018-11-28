<properties  
              pageTitle="I can't connect to my Windows VM"
              description="I can't connect to my Windows VM"
              service="microsoft.compute"
              resource="virtualmachines"
              authors="tiag"
              displayOrder="35"
              selfHelpType="resource"
              supportTopicIds="32615531"
              resourceTags="windows, windowsSQL"
              productPesIds="14749"
              cloudEnvironments="public"
/>

# I can't connect to my Windows VM

## **Recommended documents**

1. If you see RDP error due to CredSSP Encryption Oracle Remediation, please follow [this link](https://blogs.technet.microsoft.com/mckittrick/unable-to-rdp-to-virtual-machine-credssp-encryption-oracle-remediation/) for recovery steps.
2.	Restart the Virtual Machine to address startup issues by clicking 'Restart' at the top of the VM resource blade.
3. [Redeploy](data-blade:Microsoft_Azure_Compute.VirtualMachineRedeployViewModel.id.$resourceId) your VM to another host within Azure to correct any underlying platform or networking issues, which will migrate the VM to a new Azure host.
4.	If you're getting an RDP license error, use 'mstsc/admin' as a work around. If needed, uninstall or buy an RDS license.
5. Click [here](https://review.docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-vm-by-use-nested-virtualization?branch=pr-en-us-54175) to create a nested virtualization environment and mount the disk of the problem VM on the Hyper-V host (Rescue VM) for troubleshooting purposes.
6. Click [here](https://review.docs.microsoft.com/azure/virtual-machines/troubleshooting/detailed-troubleshoot-rdp?branch=pr-en-us-54175) for detailed guidelines to troubleshoot RDP connection issues.
