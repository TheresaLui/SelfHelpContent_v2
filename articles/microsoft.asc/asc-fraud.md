<properties
  pagetitle="ASC/Pending Verification due to Fraud Protection&#xD;"
  service="microsoft.certificateregistration"
  resource="certificateorders"
  ms.author="shrahman"
  selfhelptype="Generic"
  supporttopicids="32604396"
  resourcetags=""
  productpesids="16512"
  cloudenvironments="blackforest,fairfax,public,usnat,ussec,mooncake"
  disableclouds=""
  articleid="fdccae2e-f103-4a82-be97-33f6cc3a7658"
  ownershipid="Compute_AppService" />
# ASC/Pending Verification due to Fraud Protection

## **Recommended Steps**

When an App Service Certificate is marked as fraud, you'll see the error message, "Your certificate has been flagged for possible fraud. The request is currently under review." 

If the certificate is marked as fraud and has not been resolved after 24 hours, follow the steps below:

1. Go to the App Service certificate in Azure portal
2. Click **Certificate Configuration** > **Step 2: Verify** > **Domain Verification**
3. Click **Email Instructions**, which sends an email message to GoDaddy to resolve the issue

## **Recommended Documents**

* [My App Service certificate is flagged for fraud. How do I resolve this?](https://azure.github.io/AppService/2017/07/24/FAQ-SSL-certificates-for-Web-Apps-and-App-Service-Certificates#my-app-service-certificate-is-flagged-for-fraud-how-do-i-resolve-this)
