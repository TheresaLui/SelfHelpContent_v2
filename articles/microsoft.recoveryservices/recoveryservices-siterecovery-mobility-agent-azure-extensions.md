<properties
    pageTitle="I am unable to install the mobility service agent due to Azure extension issues"
    description="Questions or issues related to Azure extension installation failure, Not ready state, or update failure"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="v-miegge"
    ms.author="sideeksh"
    selfHelpType="generic"
    supportTopicIds="32744984"
    resourceTags=""
    productPesIds="16370"
    ownershipId="Compute_SiteRecovery"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="817f4ef1-1c05-4f9f-b70d-7e7cb7d3accd"
/>

# I am unable to install the mobility service agent due to Azure extension issues

## **Recommended Steps**

### Resolve the most commonly seen installation failures due to extension errors

- Resolve update failure from Azure Site Recovery extension [time-out error](https://docs.microsoft.com/azure/site-recovery/site-recovery-extension-troubleshoot#azure-site-recovery-extension-time-out)
- Resolve update failure from VM agent [unresponsive error](https://docs.microsoft.com/azure/site-recovery/site-recovery-extension-troubleshoot#protection-fails-because-the-vm-agent-is-unresponsive)
- Resolve agent update failure from site recovery extension [update or load errors](https://docs.microsoft.com/azure/site-recovery/site-recovery-extension-troubleshoot#the-site-recovery-extension-fails-to-update-or-load)
- Resolve extension failure by re-running the extension of VM through simple [powershell command](https://docs.microsoft.com/azure/virtual-machines/extensions/troubleshoot#rerun-the-extension-on-the-vm)
