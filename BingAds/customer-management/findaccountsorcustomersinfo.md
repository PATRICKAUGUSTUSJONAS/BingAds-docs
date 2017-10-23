---
title: FindAccountsOrCustomersInfo Service Operation
ms.service: bing-ads-customer-management
ms.topic: article
author: eric-urban
ms.author: eur
---
# FindAccountsOrCustomersInfo Service Operation
Gets a list of the accounts and customers that match the specified filter criteria.

## <a name="request"></a>Request Elements
The *FindAccountsOrCustomersInfoRequest* object defines the [body](#request-body) and [header](#request-header) elements of the service operation request. The elements must be in the same order as shown in the [Request SOAP](#request-soap). 

### <a name="request-body"></a>Request Body Elements

|Element|Description|Data Type|
|-----------|---------------|-------------|
|<a name="filter"></a>Filter|The criteria to use to filter the list of accounts and customers. You can specify either an account name, account number, or customer name.<br /><br />The filter value can contain a partial or full name or number. The operation includes the account or customer in the result if the name or number begins with the specified filter value.<br /><br />The operation performs a case-insensitive comparison when it compares your filter value to the name or number. For example, if you specify ?t? as the filter value, the list will include accounts and customers whose names begin with ?t? or ?T?.<br /><br />The operation filters first for accounts that match the filter criteria. If the number of accounts that match the filter criteria is less than the specified *TopN* value, the operation searches for customers whose name matches the filter criteria.<br /><br />Setting this element to an empty string is the same as calling the [GetAccountsInfo](../customer-management/getaccountsinfo.md) followed by calling the [GetCustomersInfo](../customer-management/getcustomersinfo.md).|**string**|
|<a name="topn"></a>TopN|A nonzero positive integer that specifies the number of accounts to return in the result. You must specify a value from 1 through 5,000.|**int**|
|<a name="applicationscope"></a>ApplicationScope|A value that determines whether to return advertiser accounts or publisher accounts. If you do not specify the scope, the list may include both types of accounts.|[ApplicationType](applicationtype.md)|

### <a name="request-header"></a>Request Header Elements
[!INCLUDE[request-header](./includes/request-header.md)]

## <a name="response"></a>Response Elements
The *FindAccountsOrCustomersInfoResponse* object defines the [body](#response-body) and [header](#response-header) elements of the service operation response. The elements are returned in the same order as shown in the [Response SOAP](#response-soap).

### <a name="response-body"></a>Response Body Elements

|Element|Description|Data Type|
|-----------|---------------|-------------|
|<a name="accountinfowithcustomerdata"></a>AccountInfoWithCustomerData|A list of *AccountInfoWithCustomerData* objects of the accounts and customers that match the specified filter criteria.<br /><br />The objects contain information that identifies the account and customer. To get the complete details of an account in the list, access the *AccountId* element of the *AccountInfoWithCustomerData* object and use it to call [GetAccount](../customer-management/getaccount.md) operation.<br /><br />To get the complete details of a customer in the list, access the *CustomerId* element of the *AccountInfoWithCustomerData* object and use it to call [GetCustomer](../customer-management/getcustomer.md).|[AccountInfoWithCustomerData](accountinfowithcustomerdata.md) array|

### <a name="response-header"></a>Response Header Elements
[!INCLUDE[response-header](./includes/response-header.md)]

## <a name="request-soap"></a>Request SOAP
The following template shows the order of the [body](#request-body) and [header](#request-header) elements for the SOAP request.

```xml
<s:Envelope xmlns:i="http://www.w3.org/2001/XMLSchema-instance" xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header xmlns="https://bingads.microsoft.com/Customer/v11">
    <Action mustUnderstand="1">FindAccountsOrCustomersInfo</Action>
    <ApplicationToken i:nil="false">ValueHere</ApplicationToken>
    <AuthenticationToken i:nil="false">ValueHere</AuthenticationToken>
    <DeveloperToken i:nil="false">ValueHere</DeveloperToken>
    <Password i:nil="false">ValueHere</Password>
    <UserName i:nil="false">ValueHere</UserName>
  </s:Header>
  <s:Body>
    <FindAccountsOrCustomersInfoRequest xmlns="https://bingads.microsoft.com/Customer/v11">
      <Filter i:nil="false">ValueHere</Filter>
      <TopN>ValueHere</TopN>
      <ApplicationScope i:nil="false">ValueHere</ApplicationScope>
    </FindAccountsOrCustomersInfoRequest>
  </s:Body>
</s:Envelope>
```

## <a name="response-soap"></a>Response SOAP
The following template shows the order of the [body](#response-body) and [header](#response-header) elements for the SOAP response.

```xml
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header xmlns="https://bingads.microsoft.com/Customer/v11">
    <TrackingId d3p1:nil="false" xmlns:d3p1="http://www.w3.org/2001/XMLSchema-instance">ValueHere</TrackingId>
  </s:Header>
  <s:Body>
    <FindAccountsOrCustomersInfoResponse xmlns="https://bingads.microsoft.com/Customer/v11">
      <AccountInfoWithCustomerData xmlns:e412="https://bingads.microsoft.com/Customer/v11/Entities" d4p1:nil="false" xmlns:d4p1="http://www.w3.org/2001/XMLSchema-instance">
        <e412:AccountInfoWithCustomerData>
          <e412:CustomerId d4p1:nil="false">ValueHere</e412:CustomerId>
          <e412:CustomerName d4p1:nil="false">ValueHere</e412:CustomerName>
          <e412:AccountId>ValueHere</e412:AccountId>
          <e412:AccountName d4p1:nil="false">ValueHere</e412:AccountName>
          <e412:AccountNumber d4p1:nil="false">ValueHere</e412:AccountNumber>
          <e412:AccountLifeCycleStatus>ValueHere</e412:AccountLifeCycleStatus>
          <e412:PauseReason d4p1:nil="false">ValueHere</e412:PauseReason>
        </e412:AccountInfoWithCustomerData>
      </AccountInfoWithCustomerData>
    </FindAccountsOrCustomersInfoResponse>
  </s:Body>
</s:Envelope>
```

## <a name="example"></a>Code Syntax
```csharp
protected async Task<FindAccountsOrCustomersInfoResponse> FindAccountsOrCustomersInfoAsync(
	string filter,
	int topN,
	ApplicationType applicationScope)
{
	var request = new FindAccountsOrCustomersInfoRequest
	{
		Filter = filter,
		TopN = topN,
		ApplicationScope = applicationScope
	};

	return (await CustomerManagement.CallAsync((s, r) => s.FindAccountsOrCustomersInfoAsync(r), request));
}
```
```java
static FindAccountsOrCustomersInfoResponse findAccountsOrCustomersInfo(
	string filter,
	int topN,
	ApplicationType applicationScope)
{
	FindAccountsOrCustomersInfoRequest request = new FindAccountsOrCustomersInfoRequest();

	request.setFilter(filter);
	request.setTopN(topN);
	request.setApplicationScope(applicationScope);

	return CustomerManagement.getService().findAccountsOrCustomersInfo(request);
}
```
```php
static function FindAccountsOrCustomersInfo(
	$filter,
	$topN,
	$applicationScope)

	$findAccountsOrCustomersInfoRequest = new FindAccountsOrCustomersInfoRequest();

	$request->Filter = $filter;
	$request->TopN = $topN;
	$request->ApplicationScope = $applicationScope;

	return $CustomerManagementProxy->GetService()->FindAccountsOrCustomersInfo($request);
}
```
```python
response=customermanagement.FindAccountsOrCustomersInfo(
	Filter=FilterHere,
	TopN=TopNHere,
	ApplicationScope=ApplicationScopeHere
)
```

## Requirements
Service: [CustomerManagementService.svc v11](https://clientcenter.api.bingads.microsoft.com/Api/CustomerManagement/v11/CustomerManagementService.svc)  
Namespace: https://bingads.microsoft.com/Customer/v11  
