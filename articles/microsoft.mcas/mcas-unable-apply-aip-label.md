<properties
  pageTitle="I am unable to apply an Azure Information Protection label to a file"
  description="I am unable to apply an Azure Information Protection label to a file"
  infoBubbleText=""
  service="microsoft.mcas"
  resource=""
  authors="shsagir"
  ms.author="shsagir"
  displayOrder=""
  articleId="mcas-unable-apply-aip-label"
  diagnosticScenario=""
  selfHelpType="generic"
  supportTopicIds="32728964"
  resourceTags=""
  productPesIds="16031"
  ownershipId="CloudAppSecurity_API"
  cloudEnvironments="public, fairfax, usnat, ussec"
/>

# I am unable to apply an Azure Information Protection label to a file

Most users are able to resolve Azure Information Protection labelling issues using the steps below.

## **Recommended Steps**

To use Azure Information Protection labels in Cloud App Security, make sure that:

1. You have enabled the [Office 365 app connector](https://docs.microsoft.com/cloud-app-security/connect-office-365-to-microsoft-cloud-app-security)
1. The labels are published as part of the policy. If you're using Azure Information Protection labels, the labels must be published via the Azure Information Protection portal. If you migrated to unified labels, the labels must be published via the Office 365 Security and Compliance Center.
1. You have not exceeded the default maximum of applying 100 labels per day. If you want to increase the limit, please continue with opening the ticket.
1. The file is one of the following supported types:
    * Word: docm, docx, dotm, dotx
    * Excel: xlam, xlsm, xlsx, xltx
    * PowerPoint: potm, potx, ppsx, ppsm, pptm, pptx
    * PDF (supported only with unified labeling)
1. The file is not in use
1. The file size is greater than 0 and is less than 50 MB
1. The file does not have any manually applied labels
1. The file does not have any labels applied in SharePoint Online

## **Recommended Documents**

* [Apply labels directly to files](https://docs.microsoft.com/cloud-app-security/azip-integration#apply-labels-directly-to-files)

If you're still experiencing the issue after reviewing the documentation and configuration, please continue with opening the ticket.
