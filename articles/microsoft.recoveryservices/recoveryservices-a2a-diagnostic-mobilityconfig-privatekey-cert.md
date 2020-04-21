<properties
    pageTitle="Mobility service installation failed because Private Key is not found in certificate"
    description="Mobility service installation failed because Private Key is not found in certificate"
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_A2A_MobilityAgentConfigurationFailure_PrivateKeyNotFoundInCert"
    diagnosticScenario="ASRA2AMobilityAgentConfiguratorFailure"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Mobility service installation failed because Private Key is not found in certificate

<!--issueDescription-->
Mobility service installation fails with private key not found error because the virtual machine is configured with a group policy that doesn’t allow the local system administrator to import the private key from the certificate.
<!--/issueDescription-->

## **Recommended Steps**

Contact the system administrator to obtain required permission for the local administrator to import the private key from certificate store. Refer to [Default permissions for the MachineKeys folders](https://support.microsoft.com/help/278381).
