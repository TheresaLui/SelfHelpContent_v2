<properties
    pageTitle="Azure Stack Readiness Checker"
    description="Azure Stack Readiness Checker"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629251"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
    articleId="azurestack-deploymentandregistration-readiness"
/>

# Azure Stack certificate issues

Azure Stack has a public infrastructure network using externally accessible public IP addresses assigned to a small set of Azure Stack services and possibly tenant VMs. PKI certificates with the appropriate DNS names for these Azure Stack public infrastructure endpoints are required during Azure Stack deployment.<br>

You can discover issues when you use Azure Stack Readiness Checker tool to validate Azure Stack PKI certificates. The tool checks to ensure that certificates meet the PKI requirements of an Azure Stack deployment and Azure Stack Secret Rotation, and logs the results in a report.json file. You can use the tool to validate that the generated PKI certificates are suitable for pre-deployment. You should validate certificates by leaving enough time to test and reissue certificates if necessary.<br>

## **Recommended steps**

1. Get the Azure Stack Readiness Checker tool [from the PowerShell Gallery](https://aka.ms/AzsReadinessChecker).<br>

2. Perform core services certificate validation. Follow the steps in the following procedure to prepare and to validate the Azure Stack PKI certificates for deployment and secret rotation. For more information, see [Perform core services certificate validation](https://docs.microsoft.com/azure/azure-stack/azure-stack-validate-pki-certs#perform-core-services-certificate-validation).<br>

3. Perform platform as a service certificate validation. Follow the steps in the following procedure to prepare and validate the Azure Stack PKI certificates for platform as a service (PaaS) certificates, if SQL/MySQL or App Services deployments are planned. For more information, see [Perform platform as a service certificate validation
](https://docs.microsoft.com/azure/azure-stack/azure-stack-validate-pki-certs#perform-platform-as-a-service-certificate-validation).<br>

4. Use valid certificates.
    - For deployment, securely transfer your certificates to your deployment engineer so that they can copy them onto the deployment host as specified in the [Azure Stack PKI requirements documentation](https://docs.microsoft.com/azure/azure-stack/azure-stack-pki-certs).<br>
    - For secret rotation, you can use the certificates to update old certificates for your Azure Stack environment’s public infrastructure endpoints by following the [Azure Stack Secret Rotation documentation](https://docs.microsoft.com/azure/azure-stack/azure-stack-rotate-secrets).<br>
    - For PaaS services, you can use the certificates to install SQL, MySQL, and App Services Resource Providers in Azure Stack by following the [Overview of offering services in Azure Stack documentation](https://docs.microsoft.com/azure/azure-stack/azure-stack-offer-services-overview).<br>

## **Recommended documents**

[Azure Stack public key infrastructure certificate requirements](https://docs.microsoft.com/azure/azure-stack/azure-stack-pki-certs)<br>
[Azure Stack Readiness Checker tool ](https://aka.ms/AzsReadinessChecker)