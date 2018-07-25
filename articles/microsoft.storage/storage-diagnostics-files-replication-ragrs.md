<properties
pageTitle="Replication type RA-GRS is supported on Azure Files"
description="Azure Files does not support read from secondary with RA-GRS"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
displayOrder=""
articleId="Storagev2insights_files_replicationRAGRS"
diagnosticScenario="Replication type RA-GRS is nor fully supported on Azure Files"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="public"
/>

# Replication type RA-GRS is unsupported on Azure Files

<!--issueDescription-->
Currently, Azure Files supports locally redundant storage (LRS), zone redundant storage (ZRS), and geo-redundant storage (GRS). It is possible to use read-access geo-redundant (RA-GRS) with Azure Files, but it is not possible to read from secondary. Read from secondardy will be available in the future, but we don't have timelines to share at this time.
<!--/issueDescription-->

