<properties
    pageTitle="Mobility agent cannot register with the configuration server"
    description="Mobility agent cannot register with the configuration server"
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_V2A_RegisterToCSFailure"
    diagnosticScenario="ASRV2ACSInstallFailure"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Mobility agent fails to register with the configuration server

<!--issueDescription-->
The mobility agent registration on the source machine with a configuration server fails with error **EP0886**.
<!--/issueDescription-->

## **Recommended Steps**

On the configuration server, check the log "C:\\ProgramData\\ASR\\home\\svsystems\\var\\configurator_register_host_static_info.log" and verify the cause.
