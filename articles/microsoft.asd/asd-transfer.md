<properties
	pageTitle="ASD/Transfer Domains"
	description="ASD/Transfer Domains"
	service="microsoft.asd"
	resource="asd"
	authors="cts-shrahman, cristhianu"
    ms.author="shrahman,curibe"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32604405"
	resourceTags=""
	productPesIds="16513"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="9a89a7d1-3862-484b-b8ed-90e034b6a0c7"
	ownershipId="Compute_AppService"
/>

# ASD/Transfer Domains

## **Recommended Steps**

**Transfer Domains In** <br>

* [FAQ](https://azure.github.io/AppService/2017/08/08/FAQ-App-Service-Domain-and-Custom-Domains#transfer-domain-out)

Important things to know before transferring your domain: 

* Transfer of ONLY **.COM, .NET, .ORG domain TLDs are supported** to Azure App Service Domain. We DO NOT support transfer of any other domain TLDs.
* You will NOT be charged for the domain until 7 days after the transfer is completed. The cost of the domain is the same.
* Nameservers will be updated to Azure DNS nameservers since App Service Domain uses Azure DNS to host the domain and GoDaddy as the Domain registrar
* Privacy protection will be enabled when the transfer is completed
* Domain transfer becomes void if the domain transfer was unsuccessful within 30 days

**Transfer Domains Out** <br>

* [FAQ](https://azure.github.io/AppService/2017/08/08/FAQ-App-Service-Domain-and-Custom-Domains#transfer-domain-out)
