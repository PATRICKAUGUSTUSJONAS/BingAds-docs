---
title: Customer Management Data Objects
ms.service: bing-ads-customer-management-service
ms.topic: article
author: eric-urban
ms.author: eur
description: Data objects reference for the CustomerManagement service.
---
# Customer Management Data Objects

> [!IMPORTANT]
> This v12 preview documentation is subject to change.

The Customer Management service defines the following data objects.

|Data Object|Description|
|---|---|
|[AccountInfo](accountinfo)|Defines an account identification object that contains information that identifies an account.|
|[AccountInfoWithCustomerData](accountinfowithcustomerdata)|Defines an object that contains information that identifies an account and the customer that manages or owns the account.|
|[AdApiError](adapierror)|Defines an error object that contains the details that explain why the service operation failed.|
|[AdApiFaultDetail](adapifaultdetail)|Defines a fault object that operations return when generic errors occur, such as an authentication error.|
|[Address](address)|Defines a postal address.|
|[AdvertiserAccount](advertiseraccount)|Defines an advertiser account.|
|[ApiFault](apifault)|Defines a fault object that operations return when web service-specific errors occur, such as when the request message contains incomplete or invalid data.|
|[ApplicationFault](applicationfault)|Defines the base object from which all fault detail objects derive.|
|[ClientLink](clientlink)|Defines a client link object.|
|[ContactInfo](contactinfo)|Defines the contact information for a user.|
|[Customer](customer)|Defines a customer.|
|[CustomerInfo](customerinfo)|Defines a customer identification object that contains information that identifies a customer.|
|[DateRange](daterange)|Defines a date range object.|
|[KeyValuePairOfstringstring](keyvaluepairofstringstring)|The list of key and value strings for forward compatibility to avoid otherwise breaking changes when new elements are added in the current API version.|
|[OperationError](operationerror)|Defines an error object that contains the details that explain why the service operation failed.|
|[OrderBy](orderby)|Defines an order for the list of entities returned using one of the search operations, for example [SearchAccounts](/bingads/customer-management-service/searchaccounts), [SearchClientLinks](/bingads/customer-management-service/searchclientlinks), or [SearchCustomers](/bingads/customer-management-service/searchcustomers).|
|[Paging](paging)|Defines a paging object for the list of entities returned using one of the search operations, for example [SearchAccounts](/bingads/customer-management-service/searchaccounts), [SearchClientLinks](/bingads/customer-management-service/searchclientlinks), or [SearchCustomers](/bingads/customer-management-service/searchcustomers).|
|[PersonName](personname)|Defines the name of a user.|
|[Predicate](predicate)|Defines a predicate for the list of entities requested using one of the search operations, for example [SearchAccounts](/bingads/customer-management-service/searchaccounts), [SearchClientLinks](/bingads/customer-management-service/searchclientlinks), or [SearchCustomers](/bingads/customer-management-service/searchcustomers).|
|[User](user)|Defines a user.|
|[UserInfo](userinfo)|Defines a user identification object that contains information that identifies a user.|
|[UserInvitation](userinvitation)|Defines a user invitation.|
