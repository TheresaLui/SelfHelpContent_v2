<properties
    pageTitle="I am unable to uninstall the mobility service agent"
    description="Questions or issues related to uninstallation of mobility agent"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="v-miegge"
    ms.author="sideeksh"
    selfHelpType="generic"
    supportTopicIds="32744988"
    resourceTags=""
    productPesIds="13670"
    ownershipId="Compute_SiteRecovery"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="79066d2a-4293-45ba-a81e-5c64194c3aca"
/>

# I am unable to uninstall the mobility service agent

## Unable to remove mobility agent on protected machine

- You can choose to uninstall or disable ASR through a simple powershell command:

  - For Azure to Azure, [disable replication](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-powershell#disable-replication)
  - For V2A, [uninstall the mobility service](https://docs.microsoft.com/azure/site-recovery/vmware-physical-manage-mobility-service#uninstall-mobility-service)

- To fix the errors in replication & continue Disaster Recovery of your machine:

  - For Azure to Azure, ensure that there are no [connectivity errors](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-network-connectivity)
  
  - For V2A, ensure that all ASR infrastructure is healthy:
  
    - [Troubleshoot replication issues for VMware VMs and physical servers](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication)
    - [Troubleshoot configuration server issues](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-configuration-server)

## HyperV to Azure

- Ensure that there are no [performance issues](https://docs.microsoft.com/azure/site-recovery/hyper-v-azure-troubleshoot)
