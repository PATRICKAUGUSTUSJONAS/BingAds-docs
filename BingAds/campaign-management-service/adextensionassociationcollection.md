---
title: AdExtensionAssociationCollection Data Object - Campaign Management
ms.service: bing-ads-campaign-management-service
ms.topic: article
author: eric-urban
ms.author: eur
description: Defines an array of objects that associate an ad extension and its editorial status to an account, campaign, or ad group.
---
# AdExtensionAssociationCollection Data Object - Campaign Management
Defines an array of objects that associate an ad extension and its editorial status to an account, campaign, or ad group.

## Syntax
```xml
<xs:complexType name="AdExtensionAssociationCollection" xmlns:xs="http://www.w3.org/2001/XMLSchema">
  <xs:sequence>
    <xs:element name="AdExtensionAssociations" nillable="true" type="tns:ArrayOfAdExtensionAssociation" />
  </xs:sequence>
</xs:complexType>
```

## <a name="elements"></a>Elements

|Element|Description|Data Type|
|-----------|---------------|-------------|
|<a name="adextensionassociations"></a>AdExtensionAssociations|An array of objects that associate an ad extension and its editorial status to an account, campaign, or ad group.<br/><br/>**Add:** Required<br/>**Update:** Required|[AdExtensionAssociation](adextensionassociation.md) array|

## Requirements
Service: [CampaignManagementService.svc v11](https://campaign.api.bingads.microsoft.com/Api/Advertiser/CampaignManagement/v11/CampaignManagementService.svc)  
Namespace: https\://bingads.microsoft.com/CampaignManagement/v11  

## Used By
[GetAdExtensionsAssociations](getadextensionsassociations.md)  
