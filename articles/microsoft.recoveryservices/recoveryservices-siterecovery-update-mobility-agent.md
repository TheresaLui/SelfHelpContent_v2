<properties
    pageTitle="I am unable to update the mobility service agent"
    description="Questions or issues related to mobility agent update"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="v-miegge"
    ms.author="sideeksh"
    selfHelpType="generic"
    supportTopicIds="32744989"
    resourceTags=""
    productPesIds="13670"
    ownershipId="Compute_SiteRecovery"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="1ff9926f-f513-4f2c-b29a-af993d7960ef"
/>

# I am unable to update the mobility service agent

## **Recommended Steps**

### Troubleshoot the most commonly seen mobility agent update errors

- Update failure due to Azure Site Recovery extension [time-out error](https://docs.microsoft.com/azure/site-recovery/site-recovery-extension-troubleshoot#azure-site-recovery-extension-time-out)
- Update failure due to VM agent [unresponsive error](https://docs.microsoft.com/azure/site-recovery/site-recovery-extension-troubleshoot#protection-fails-because-the-vm-agent-is-unresponsive)
- Update completed with [reboot warnings](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#install-mobility-service-completed-with-warning-to-reboot-errorid-95265--95266)

### Mobility agent update failed as the current version is older than the supported version

- Refer to [our guidance](https://docs.microsoft.com/azure/site-recovery/service-updates-how-to#vmware-vmphysical-server-disaster-recovery-to-azure) to update ASR infrastructure mobility agent to the latest versions without errors)
- Enable automatic updates on Azure VM to [stay on latest version without manual intervention](https://docs.microsoft.com/azure/site-recovery/service-updates-how-to#azure-vm-disaster-recovery-to-azure)
