<properties
	  pageTitle="Syslog configuration"
	  description="Syslog configuration"
      service="Microsoft.Security"
      resource="Microsoft.Security/alerts"
	  authors="rimayber"
	  ms.author="rimayber"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="1f2af6c0-ea47-4cbd-9136-a378398ed6c8"
	  ownershipId="Azure_Sentinel"
/>

# Syslog configuration

Changes to syslog configuration are being overwritten. The following command ensures that the configuration change you made in the previous step does not get overwritten.
sudo su omsagent -c 'python /opt/microsoft/omsconfig/Scripts/OMS_MetaConfigHelper.py --disable'	

