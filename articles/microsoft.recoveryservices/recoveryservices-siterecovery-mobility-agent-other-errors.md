<properties
  pagetitle="I am unable to install the mobility service agent due to other errors&#xD;"
  description="Questions or issues related to mobility agent installation failure"
  service="microsoft.recoveryservices"
  resource="vaults"
  ms.author="sideeksh,sharrai"
  selfhelptype="Generic"
  supporttopicids="32744986"
  resourcetags=""
  productpesids="16370"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="e3784e38-589f-4fb2-aa20-360ea40fc5a3"
  ownershipid="Compute_SiteRecovery" />
# I am unable to install the mobility service agent due to other errors

Resolve most issues that occur when installing mobility service agent by following these steps.

## **Recommended Steps**

- Ensure that there are no antivirus programs, like Carbon Black, blocking the installation of mobility service on your machine. If there are, then disable them before retrying the installation.
- Ensure that .NET version 4.6.2 has been installed on your machines
- If your source machine is a VMware machine, then ensure that the credentials provided for installing mobility service have the required access. It is recommended to use credentials with administrator privileges for Windows machines or root user for Linux machines. [Learn more](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server#add-credentials-for-mobility-service-installation) about how to add/modify the accounts.
- For VMware machines, ensure that the [File and Printer sharing service is enabled](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#file-and-printer-sharing-services-check-errorid-95105--95106) and [WMI service is enabled](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#windows-management-instrumentation-wmi-configuration-check-error-code-95103) on your virtual machine. Also ensure that the [network shared folders on your virtual machine are accessible](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#check-access-for-network-shared-folders-on-source-machine-errorid-9510595523) from the process server.
- For VMware machines, you can install the mobility service manually by using [these instructions](https://docs.microsoft.com/azure/site-recovery/vmware-physical-mobility-service-overview#install-the-mobility-service-using-ui)
