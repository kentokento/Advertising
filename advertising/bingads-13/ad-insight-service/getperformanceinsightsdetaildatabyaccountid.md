---
title: GetPerformanceInsightsDetailDataByAccountId Service Operation - Ad Insight
ms.service: bing-ads-ad-insight-service
ms.topic: article
author: rgaritta
ms.author: v-rgaritta
description: Gets the performance insights detail data for a single account.
dev_langs: 
  - csharp
  - java
  - php
  - python
---
# GetPerformanceInsightsDetailDataByAccountId Service Operation - Ad Insight
Gets the performance insights detail data for a single account.

## <a name="request"></a>Request Elements
The *GetPerformanceInsightsDetailDataByAccountIdRequest* object defines the [body](#request-body) and [header](#request-header) elements of the service operation request. The elements must be in the same order as shown in the [Request SOAP](#request-soap). 

> [!NOTE]
> Unless otherwise noted below, all request elements are required.

### <a name="request-body"></a>Request Body Elements

|Element|Description|Data Type|
|-----------|---------------|-------------|
|<a name="enddate"></a>EndDate|The end date range for performance insights. The maximum date range is one month.|[DayMonthAndYear](daymonthandyear.md)|
|<a name="entitytype"></a>EntityType|The entity level that you want to request performance insights summary data from. We currently support *account* and *campaign* level data.|[EntityType](entitytype.md)|
|<a name="startdate"></a>StartDate|The start date range for performance insights.|[DayMonthAndYear](daymonthandyear.md)|

### <a name="request-header"></a>Request Header Elements
[!INCLUDE[request-header](./includes/request-header.md)]

## <a name="response"></a>Response Elements
The *GetPerformanceInsightsDetailDataByAccountIdResponse* object defines the [body](#response-body) and [header](#response-header) elements of the service operation response. The elements are returned in the same order as shown in the [Response SOAP](#response-soap).

### <a name="response-body"></a>Response Body Elements

|Element|Description|Data Type|
|-----------|---------------|-------------|
|<a name="result"></a>Result|Defines the performance insight results from calling the [GetPerformanceInsightsDetailDataByAccountId](getperformanceinsightsdetaildatabyaccountid.md) operation.|[PerformanceInsightsDetail](performanceinsightsdetail.md) array|

### <a name="response-header"></a>Response Header Elements
[!INCLUDE[response-header](./includes/response-header.md)]

## <a name="request-soap"></a>Request SOAP
This template was generated by a tool to show the [order](../guides/services-protocol.md#element-order) of the [body](#request-body) and [header](#request-header) elements for the SOAP request. For supported types that you can use with this service operation, see the [Request Body Elements](#request-body) reference above.

```xml
<s:Envelope xmlns:i="http://www.w3.org/2001/XMLSchema-instance" xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header xmlns="https://bingads.microsoft.com/AdInsight/v13">
    <Action mustUnderstand="1">GetPerformanceInsightsDetailDataByAccountId</Action>
    <AuthenticationToken i:nil="false">ValueHere</AuthenticationToken>
    <CustomerAccountId i:nil="false">ValueHere</CustomerAccountId>
    <CustomerId i:nil="false">ValueHere</CustomerId>
    <DeveloperToken i:nil="false">ValueHere</DeveloperToken>
  </s:Header>
  <s:Body>
    <GetPerformanceInsightsDetailDataByAccountIdRequest xmlns="https://bingads.microsoft.com/AdInsight/v13">
      <EntityType>ValueHere</EntityType>
      <StartDate i:nil="false">
        <Day>ValueHere</Day>
        <Month>ValueHere</Month>
        <Year>ValueHere</Year>
      </StartDate>
      <EndDate i:nil="false">
        <Day>ValueHere</Day>
        <Month>ValueHere</Month>
        <Year>ValueHere</Year>
      </EndDate>
    </GetPerformanceInsightsDetailDataByAccountIdRequest>
  </s:Body>
</s:Envelope>
```

## <a name="response-soap"></a>Response SOAP
This template was generated by a tool to show the order of the [body](#response-body) and [header](#response-header) elements for the SOAP response.

```xml
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header xmlns="https://bingads.microsoft.com/AdInsight/v13">
    <TrackingId d3p1:nil="false" xmlns:d3p1="http://www.w3.org/2001/XMLSchema-instance">ValueHere</TrackingId>
  </s:Header>
  <s:Body>
    <GetPerformanceInsightsDetailDataByAccountIdResponse xmlns="https://bingads.microsoft.com/AdInsight/v13">
      <Result d4p1:nil="false" xmlns:d4p1="http://www.w3.org/2001/XMLSchema-instance">
        <PerformanceInsightsDetail>
          <EntityId>ValueHere</EntityId>
          <EntityType>ValueHere</EntityType>
          <KPIType>ValueHere</KPIType>
          <Date d4p1:nil="false">
            <Day>ValueHere</Day>
            <Month>ValueHere</Month>
            <Year>ValueHere</Year>
          </Date>
          <Description d4p1:nil="false">
            <TemplateId>ValueHere</TemplateId>
            <Parameters d4p1:nil="false">
              <PerformanceInsightsMessageParameter d4p1:type="-- derived type specified here with the appropriate prefix --">
                <Type>ValueHere</Type>
                <!--This field is applicable if the derived type attribute is set to TextParameter-->
                <SuggestedText d4p1:nil="false">ValueHere</SuggestedText>
                <!--These fields are applicable if the derived type attribute is set to UrlParameter-->
                <SuggestedText d4p1:nil="false">ValueHere</SuggestedText>
                <SuggestedUrl d4p1:nil="false">ValueHere</SuggestedUrl>
                <UrlCategory>ValueHere</UrlCategory>
                <UrlId>ValueHere</UrlId>
                <!--These fields are applicable if the derived type attribute is set to EntityParameter-->
                <EntityCount>ValueHere</EntityCount>
                <EntityDetails d4p1:nil="false">
                  <EntityDetail>
                    <EntityId>ValueHere</EntityId>
                    <EntityName d4p1:nil="false">ValueHere</EntityName>
                  </EntityDetail>
                </EntityDetails>
                <EntityType>ValueHere</EntityType>
                <SuggestedText d4p1:nil="false">ValueHere</SuggestedText>
              </PerformanceInsightsMessageParameter>
            </Parameters>
            <IndentationLevel>ValueHere</IndentationLevel>
          </Description>
          <RootCauses d4p1:nil="false">
            <PerformanceInsightsMessage>
              <TemplateId>ValueHere</TemplateId>
              <Parameters d4p1:nil="false">
                <PerformanceInsightsMessageParameter d4p1:type="-- derived type specified here with the appropriate prefix --">
                  <Type>ValueHere</Type>
                  <!--This field is applicable if the derived type attribute is set to TextParameter-->
                  <SuggestedText d4p1:nil="false">ValueHere</SuggestedText>
                  <!--These fields are applicable if the derived type attribute is set to UrlParameter-->
                  <SuggestedText d4p1:nil="false">ValueHere</SuggestedText>
                  <SuggestedUrl d4p1:nil="false">ValueHere</SuggestedUrl>
                  <UrlCategory>ValueHere</UrlCategory>
                  <UrlId>ValueHere</UrlId>
                  <!--These fields are applicable if the derived type attribute is set to EntityParameter-->
                  <EntityCount>ValueHere</EntityCount>
                  <EntityDetails d4p1:nil="false">
                    <EntityDetail>
                      <EntityId>ValueHere</EntityId>
                      <EntityName d4p1:nil="false">ValueHere</EntityName>
                    </EntityDetail>
                  </EntityDetails>
                  <EntityType>ValueHere</EntityType>
                  <SuggestedText d4p1:nil="false">ValueHere</SuggestedText>
                </PerformanceInsightsMessageParameter>
              </Parameters>
              <IndentationLevel>ValueHere</IndentationLevel>
            </PerformanceInsightsMessage>
          </RootCauses>
          <Actions d4p1:nil="false">
            <PerformanceInsightsMessage>
              <TemplateId>ValueHere</TemplateId>
              <Parameters d4p1:nil="false">
                <PerformanceInsightsMessageParameter d4p1:type="-- derived type specified here with the appropriate prefix --">
                  <Type>ValueHere</Type>
                  <!--This field is applicable if the derived type attribute is set to TextParameter-->
                  <SuggestedText d4p1:nil="false">ValueHere</SuggestedText>
                  <!--These fields are applicable if the derived type attribute is set to UrlParameter-->
                  <SuggestedText d4p1:nil="false">ValueHere</SuggestedText>
                  <SuggestedUrl d4p1:nil="false">ValueHere</SuggestedUrl>
                  <UrlCategory>ValueHere</UrlCategory>
                  <UrlId>ValueHere</UrlId>
                  <!--These fields are applicable if the derived type attribute is set to EntityParameter-->
                  <EntityCount>ValueHere</EntityCount>
                  <EntityDetails d4p1:nil="false">
                    <EntityDetail>
                      <EntityId>ValueHere</EntityId>
                      <EntityName d4p1:nil="false">ValueHere</EntityName>
                    </EntityDetail>
                  </EntityDetails>
                  <EntityType>ValueHere</EntityType>
                  <SuggestedText d4p1:nil="false">ValueHere</SuggestedText>
                </PerformanceInsightsMessageParameter>
              </Parameters>
              <IndentationLevel>ValueHere</IndentationLevel>
            </PerformanceInsightsMessage>
          </Actions>
        </PerformanceInsightsDetail>
      </Result>
    </GetPerformanceInsightsDetailDataByAccountIdResponse>
  </s:Body>
</s:Envelope>
```

## <a name="example"></a>Code Syntax
The example syntax can be used with [Bing Ads SDKs](../guides/client-libraries.md). See [Bing Ads API Code Examples](../guides/code-examples.md) for more examples.
```csharp
public async Task<GetPerformanceInsightsDetailDataByAccountIdResponse> GetPerformanceInsightsDetailDataByAccountIdAsync(
	EntityType entityType,
	DayMonthAndYear startDate,
	DayMonthAndYear endDate)
{
	var request = new GetPerformanceInsightsDetailDataByAccountIdRequest
	{
		EntityType = entityType,
		StartDate = startDate,
		EndDate = endDate
	};

	return (await AdInsightService.CallAsync((s, r) => s.GetPerformanceInsightsDetailDataByAccountIdAsync(r), request));
}
```
```java
static GetPerformanceInsightsDetailDataByAccountIdResponse getPerformanceInsightsDetailDataByAccountId(
	EntityType entityType,
	DayMonthAndYear startDate,
	DayMonthAndYear endDate) throws RemoteException, Exception
{
	GetPerformanceInsightsDetailDataByAccountIdRequest request = new GetPerformanceInsightsDetailDataByAccountIdRequest();

	request.setEntityType(entityType);
	request.setStartDate(startDate);
	request.setEndDate(endDate);

	return AdInsightService.getService().getPerformanceInsightsDetailDataByAccountId(request);
}
```
```php
static function GetPerformanceInsightsDetailDataByAccountId(
	$entityType,
	$startDate,
	$endDate)
{

	$GLOBALS['Proxy'] = $GLOBALS['AdInsightProxy'];

	$request = new GetPerformanceInsightsDetailDataByAccountIdRequest();

	$request->EntityType = $entityType;
	$request->StartDate = $startDate;
	$request->EndDate = $endDate;

	return $GLOBALS['AdInsightProxy']->GetService()->GetPerformanceInsightsDetailDataByAccountId($request);
}
```
```python
response=adinsight_service.GetPerformanceInsightsDetailDataByAccountId(
	EntityType=EntityType,
	StartDate=StartDate,
	EndDate=EndDate)
```

## Requirements
Service: [AdInsightService.svc v13](https://adinsight.api.bingads.microsoft.com/Api/Advertiser/AdInsight/v13/AdInsightService.svc)  
Namespace: https\://bingads.microsoft.com/AdInsight/v13  
