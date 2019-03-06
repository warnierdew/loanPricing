# PricingApi

All URIs are relative to *https://petstore.swagger.io/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**updatePricingIdWithForm**](PricingApi.md#updatePricingIdWithForm) | **POST** /pricing | Updates a Pricing form data


<a name="updatePricingIdWithForm"></a>
# **updatePricingIdWithForm**
> Pricing updatePricingIdWithForm(body)

Updates a Pricing form data



### Example
```java
// Import classes:
//import eu.eisti.calculation.client.invoker.ApiException;
//import eu.eisti.calculation.client.api.PricingApi;


PricingApi apiInstance = new PricingApi();
PricingCriteria body = new PricingCriteria(); // PricingCriteria | ID of PricingId that needs to be updated
try {
    Pricing result = apiInstance.updatePricingIdWithForm(body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling PricingApi#updatePricingIdWithForm");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**PricingCriteria**](PricingCriteria.md)| ID of PricingId that needs to be updated |

### Return type

[**Pricing**](Pricing.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

