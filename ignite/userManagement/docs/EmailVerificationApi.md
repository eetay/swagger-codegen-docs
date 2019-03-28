# EmailVerificationApi

All URIs are relative to *https://ignitesrv5:30004*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getIsEmailVerifiedUsingGET**](EmailVerificationApi.md#getIsEmailVerifiedUsingGET) | **GET** /v1/emailVerification/{userId}/isEmailVerified | Get if user email was verified by user id
[**resendEmailVerificationUsingPUT**](EmailVerificationApi.md#resendEmailVerificationUsingPUT) | **PUT** /v1/emailVerification/{userId}/resendEmailVerification | Resend email verification
[**verifyEmailUsingGET**](EmailVerificationApi.md#verifyEmailUsingGET) | **GET** /v1/emailVerification/{token} | Verify user&#39;s email


<a name="getIsEmailVerifiedUsingGET"></a>
# **getIsEmailVerifiedUsingGET**
> EmailVerificationRepresentation getIsEmailVerifiedUsingGET(userId, correlationId)

Get if user email was verified by user id

Get if user email was verified by user id.  

### Example
```java
// Import classes:
//import io.swagger.userManagement.ApiException;
//import io.swagger.userManagement.api.EmailVerificationApi;


EmailVerificationApi apiInstance = new EmailVerificationApi();
String userId = "userId_example"; // String | User ID
String correlationId = "correlationId_example"; // String | Correlation ID
try {
    EmailVerificationRepresentation result = apiInstance.getIsEmailVerifiedUsingGET(userId, correlationId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EmailVerificationApi#getIsEmailVerifiedUsingGET");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userId** | **String**| User ID |
 **correlationId** | **String**| Correlation ID |

### Return type

[**EmailVerificationRepresentation**](EmailVerificationRepresentation.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, */*

<a name="resendEmailVerificationUsingPUT"></a>
# **resendEmailVerificationUsingPUT**
> resendEmailVerificationUsingPUT(userId, correlationId)

Resend email verification

Verify a user by a token

### Example
```java
// Import classes:
//import io.swagger.userManagement.ApiException;
//import io.swagger.userManagement.api.EmailVerificationApi;


EmailVerificationApi apiInstance = new EmailVerificationApi();
String userId = "userId_example"; // String | userId
String correlationId = "correlationId_example"; // String | Correlation ID
try {
    apiInstance.resendEmailVerificationUsingPUT(userId, correlationId);
} catch (ApiException e) {
    System.err.println("Exception when calling EmailVerificationApi#resendEmailVerificationUsingPUT");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userId** | **String**| userId |
 **correlationId** | **String**| Correlation ID |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

<a name="verifyEmailUsingGET"></a>
# **verifyEmailUsingGET**
> BaseRepresentation verifyEmailUsingGET(token, correlationId)

Verify user&#39;s email

Verify a user by a token

### Example
```java
// Import classes:
//import io.swagger.userManagement.ApiException;
//import io.swagger.userManagement.api.EmailVerificationApi;


EmailVerificationApi apiInstance = new EmailVerificationApi();
String token = "token_example"; // String | token
String correlationId = "correlationId_example"; // String | Correlation ID
try {
    BaseRepresentation result = apiInstance.verifyEmailUsingGET(token, correlationId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EmailVerificationApi#verifyEmailUsingGET");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **token** | **String**| token |
 **correlationId** | **String**| Correlation ID |

### Return type

[**BaseRepresentation**](BaseRepresentation.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

