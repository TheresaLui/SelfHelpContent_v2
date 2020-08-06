<properties
  pageTitle="I'm having a problem with setting up or getting data from my log collector"
  description="I'm having a problem with setting up or getting data from my log collector"
  infoBubbleText=""
  service="microsoft.mcas"
  resource=""
  authors="shsagir"
  ms.author="shsagir"
  displayOrder=""
  articleId="mcas-cloud-discovery-data"
  diagnosticScenario=""
  selfHelpType="generic"
  supportTopicIds="32728969, 32728972"
  resourceTags=""
  productPesIds="16031"
  ownershipId="CloudAppSecurity_Discovery"
  cloudEnvironments="public, fairfax, usnat, ussec"
/>

# I'm having a problem with setting up or getting data from my log collector

Most users are able to resolve log collector issues using the steps below.

## **Recommended Steps**

Check that your log collector is set up correctly

1. Make sure you are using one of the operating systems supported by Cloud App Security: [Docker for Windows](https://docs.microsoft.com/cloud-app-security/discovery-docker-windows), [Linux on premise](https://docs.microsoft.com/cloud-app-security/discovery-docker-ubuntu), [Docker for Linux on Azure](https://docs.microsoft.com/cloud-app-security/discovery-docker-ubuntu-azure)
1. Verify that the host machine has sufficient capacity:
    - Disk space: 250 GB
    - CPU: 2
    - RAM: 4 GB
1. For Windows log collectors only: verify that virtualization on the operating system enabled with Hyper-V

Check that your network is set up correctly

1. Verify that the log collector has permissions to:
    - Receive inbound FTP and Syslog traffic
    - Initiate outbound traffic to the portal (for example *contoso\.cloudappsecurity\.com*) on port 443
    - Initiate outbound traffic to the Azure blob storage on port 443? For more information, see [Log collector network requirements](https://docs.microsoft.com/cloud-app-security/network-requirements#log-collector).
1. For log collectors not using a proxy server - Verify that you allowed HTTP connections to *http\:\/\/ocsp\.msocsp\.com\/* and *http\:\/\/ocsp.digicert.com\/* on port 80

**Troubleshooting**

1. Are you having an issue uploading log files? Verify that your:

    - Host machine has sufficient empty disk space
    - Log collector has not exceeded the 50 GB per hour upload capacity. For more information, see [Log collector performance](https://docs.microsoft.com/cloud-app-security/discovery-docker-windows#log-collector-performance).

1. Are you having an issue processing log files?

    - Check that the log file you are uploading matches the sample you uploaded to Cloud App Security. For more information the format for log files, see [Using traffic logs for Cloud Discovery](https://docs.microsoft.com/cloud-app-security/create-snapshot-cloud-discovery-reports#using-traffic-logs-for-cloud-discovery-).

If you're still experiencing the issue after reviewing the documentation and configuration, please continue with opening the ticket.
