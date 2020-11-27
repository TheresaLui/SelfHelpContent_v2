<properties pageTitle="TSG Summary: File Sync sync issue"
            description="TSG Summary: File Sync sync issue"
            service="Microsoft.Storage"
            resource="Microsoft.Storage/storageAccounts"
            authors="JRMayberry"
            ms.author="rimayber"
            displayOrder=""
            selfHelpType="TSG_Description"
            supportTopicIds=""
            resourceTags=""
            productPesIds=""
            cloudEnvironments="public, fairfax, usnat, ussec"
            articleId="5f51d199-7827-4aa6-aa4b-d5cdd7865d42"
            ownershipId="Centennial_CloudNet_LoadBalancer" />

# File Sync sync issue

This troubleshooter will guide you to find the root cause and resolution for customers experiencing issues with Azure File Sync Errors.

## Jarvis File Sync Dashboards

Please use the below dashboards to perform in-depth troubleshooting with any Azure File Sync scenario.

|Dashboard       |Description                    
|----------------|-------------------------------
|[Tiering and Recall](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fjarvis-west.dc.ad.msft.net%2Fdashboard%2FXEEE-Dashboards%2FFileSync%2FTiering%252520and%252520Recall&data=02%7C01%7Cdroltean%40microsoft.com%7Cb10a9d3d669a4499e1b108d85be2bee8%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637360376738431233&sdata=E3tWbSS7XpFY42%2F%2FigkGVz0YYa%2B6LP%2FVsETkzuN4VDA%3D&reserved=0)|Used for Sync Tiering & Recall scenarios when Cloud Tiering is On.           
|[Sync Progress & Performance](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fjarvis-west.dc.ad.msft.net%2Fdashboard%2FXEEE-Dashboards%2FFileSync%2FSync%252520Progress%252520%252526%252520Performance&data=02%7C01%7Cdroltean%40microsoft.com%7Cb10a9d3d669a4499e1b108d85be2bee8%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637360376738441190&sdata=7RlKn%2FH5K9wmvOCVPFyvjATEjFb58KpXCi8JRA0gFoY%3D&reserved=0)|Used for tracking Sync Progress - both Upload & Download scenarios from SEP as well as Cloud-side Enumeration.            
|[SEP Health](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fjarvis-west.dc.ad.msft.net%2Fdashboard%2FXEEE-Dashboards%2FFileSync%2FSEP%252520Health&data=02%7C01%7Cdroltean%40microsoft.com%7Cb10a9d3d669a4499e1b108d85be2bee8%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637360376738441190&sdata=8WJdLcSrEfIEZysiKDGfR5OyI3WFbRa6QZ7QFYb6zYo%3D&reserved=0)|Used for viewing Agent & Filter details on SEP.
|[AFS Management](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fjarvis-west.dc.ad.msft.net%2Fdashboard%2FXEEE-Dashboards%2FFileSync%2FAFS%252520Management&data=02%7C01%7Cdroltean%40microsoft.com%7Cb10a9d3d669a4499e1b108d85be2bee8%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637360376738441190&sdata=rXoJTp53%2FkfZLcUhiaImlyAs6r%2FGvnXTSNuHCOSZcco%3D&reserved=0)|Used for viewing AFS Management operations.
