<properties
    pageTitle="Push installation of mobility agent fails due to configuration file corruption"
    description="Registration of mobility agent with configuration server has failed because the platform value is set to NULL."
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_V2A_PushInstallFailure_ConfigFileCorrupt"
    diagnosticScenario="ASRV2APushInstallFailure"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Push installation of mobility agent fails due to configuration file corruption

<!--issueDescription-->
The registration of the mobility agent with a configuration server fails because the platform value is set to NULL.
<!--/issueDescription-->

## **Recommended Steps**

Uninstall the mobility agent from source machine and perform a fresh installation. If the uninstallation fails, follow these steps:

- Open the file Installation_Directory/uninstall.sh and comment out the call to the StopServices function
- Open the file Installation_Directory/Vx/bin/uninstall and comment out the call to the stop_services function
- Open the file Installation_Directory/Fx/uninstall and comment out the complete section that's trying to stop the Fx service
- Uninstall the mobility agent
- Reboot the system and try to install the agent again
