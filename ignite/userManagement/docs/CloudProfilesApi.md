# CloudProfilesApi

All URIs are relative to *https://ignitesrv5:30004*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addCloudProfileUsingPOST**](CloudProfilesApi.md#addCloudProfileUsingPOST) | **POST** /v1/users/cloudprofile | Add a new cloud profile
[**deleteCloudProfileUsingDELETE**](CloudProfilesApi.md#deleteCloudProfileUsingDELETE) | **DELETE** /v1/users/cloudprofile/{id} | Delete a cloud profile
[**editCloudProfileUsingPATCH**](CloudProfilesApi.md#editCloudProfileUsingPATCH) | **PATCH** /v1/users/cloudprofile/{id} | Edit a cloud profile
[**getCloudProfileUsingGET**](CloudProfilesApi.md#getCloudProfileUsingGET) | **GET** /v1/users/cloudprofile/{userId}/{profileName} | Get cloud profile by business key
[**getCloudProfilesUsingGET**](CloudProfilesApi.md#getCloudProfilesUsingGET) | **GET** /v1/users/cloudprofile/{userId} | Get simplified cloud profiles by user id
[**updateCloudProfileUsingPUT**](CloudProfilesApi.md#updateCloudProfileUsingPUT) | **PUT** /v1/users/cloudprofile/{id} | Update a full cloud profile


<a name="addCloudProfileUsingPOST"></a>
# **addCloudProfileUsingPOST**
> CloudProfileListRepresentation addCloudProfileUsingPOST(correlationId, requestPayload)

Add a new cloud profile

Creates a cloud profile for user.   

### Example
```java
// Import classes:
//import io.swagger.userManagement.ApiException;
//import io.swagger.userManagement.api.CloudProfilesApi;


CloudProfilesApi apiInstance = new CloudProfilesApi();
String correlationId = "correlationId_example"; // String | Correlation ID
CloudProfileRequest requestPayload = new CloudProfileRequest(); // CloudProfileRequest | Parameters that define a cloud profile
try {
    CloudProfileListRepresentation result = apiInstance.addCloudProfileUsingPOST(correlationId, requestPayload);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling CloudProfilesApi#addCloudProfileUsingPOST");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **correlationId** | **String**| Correlation ID |
 **requestPayload** | [**CloudProfileRequest**](CloudProfileRequest.md)| Parameters that define a cloud profile | [optional]

### Return type

[**CloudProfileListRepresentation**](CloudProfileListRepresentation.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="deleteCloudProfileUsingDELETE"></a>
# **deleteCloudProfileUsingDELETE**
> CloudProfileListRepresentation deleteCloudProfileUsingDELETE(id, correlationId)

Delete a cloud profile

Delete a cloud profile for user.

### Example
```java
// Import classes:
//import io.swagger.userManagement.ApiException;
//import io.swagger.userManagement.api.CloudProfilesApi;


CloudProfilesApi apiInstance = new CloudProfilesApi();
String id = "id_example"; // String | id
String correlationId = "correlationId_example"; // String | Correlation ID
try {
    CloudProfileListRepresentation result = apiInstance.deleteCloudProfileUsingDELETE(id, correlationId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling CloudProfilesApi#deleteCloudProfileUsingDELETE");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| id |
 **correlationId** | **String**| Correlation ID |

### Return type

[**CloudProfileListRepresentation**](CloudProfileListRepresentation.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="editCloudProfileUsingPATCH"></a>
# **editCloudProfileUsingPATCH**
> CloudProfileListRepresentation editCloudProfileUsingPATCH(id, correlationId, requestPayload)

Edit a cloud profile

Updates a cloud profile for user.  This update edits or adds specific fields. For full profile override use PUT  

### Example
```java
// Import classes:
//import io.swagger.userManagement.ApiException;
//import io.swagger.userManagement.api.CloudProfilesApi;


CloudProfilesApi apiInstance = new CloudProfilesApi();
String id = "id_example"; // String | id
String correlationId = "correlationId_example"; // String | Correlation ID
CloudProfilePatch requestPayload = new CloudProfilePatch(); // CloudProfilePatch | Parameters that define a cloud profile
try {
    CloudProfileListRepresentation result = apiInstance.editCloudProfileUsingPATCH(id, correlationId, requestPayload);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling CloudProfilesApi#editCloudProfileUsingPATCH");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| id |
 **correlationId** | **String**| Correlation ID |
 **requestPayload** | [**CloudProfilePatch**](CloudProfilePatch.md)| Parameters that define a cloud profile | [optional]

### Return type

[**CloudProfileListRepresentation**](CloudProfileListRepresentation.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getCloudProfileUsingGET"></a>
# **getCloudProfileUsingGET**
> CloudProfileListRepresentation getCloudProfileUsingGET(userId, profileName, correlationId)

Get cloud profile by business key

Gets cloud profile by user id and profile name.   

### Example
```java
// Import classes:
//import io.swagger.userManagement.ApiException;
//import io.swagger.userManagement.api.CloudProfilesApi;


CloudProfilesApi apiInstance = new CloudProfilesApi();
String userId = "userId_example"; // String | User ID
String profileName = "profileName_example"; // String | Profile name
String correlationId = "correlationId_example"; // String | Correlation ID
try {
    CloudProfileListRepresentation result = apiInstance.getCloudProfileUsingGET(userId, profileName, correlationId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling CloudProfilesApi#getCloudProfileUsingGET");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userId** | **String**| User ID |
 **profileName** | **String**| Profile name |
 **correlationId** | **String**| Correlation ID |

### Return type

[**CloudProfileListRepresentation**](CloudProfileListRepresentation.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getCloudProfilesUsingGET"></a>
# **getCloudProfilesUsingGET**
> Map&lt;String, String&gt; getCloudProfilesUsingGET(userId, correlationId)

Get simplified cloud profiles by user id

Gets simplified list of cloud profiles by user id.  

### Example
```java
// Import classes:
//import io.swagger.userManagement.ApiException;
//import io.swagger.userManagement.api.CloudProfilesApi;


CloudProfilesApi apiInstance = new CloudProfilesApi();
String userId = "userId_example"; // String | User ID
String correlationId = "correlationId_example"; // String | Correlation ID
try {
    Map<String, String> result = apiInstance.getCloudProfilesUsingGET(userId, correlationId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling CloudProfilesApi#getCloudProfilesUsingGET");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userId** | **String**| User ID |
 **correlationId** | **String**| Correlation ID |

### Return type

**Map&lt;String, String&gt;**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="updateCloudProfileUsingPUT"></a>
# **updateCloudProfileUsingPUT**
> CloudProfileListRepresentation updateCloudProfileUsingPUT(id, correlationId, requestPayload)

Update a full cloud profile

Updates a cloud profile for user.  This update overrides the entire profile. For partial update use PATCH  

### Example
```java
// Import classes:
//import io.swagger.userManagement.ApiException;
//import io.swagger.userManagement.api.CloudProfilesApi;


CloudProfilesApi apiInstance = new CloudProfilesApi();
String id = "id_example"; // String | id
String correlationId = "correlationId_example"; // String | Correlation ID
CloudProfileRequest requestPayload = new CloudProfileRequest(); // CloudProfileRequest | Parameters that define a cloud profile
try {
    CloudProfileListRepresentation result = apiInstance.updateCloudProfileUsingPUT(id, correlationId, requestPayload);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling CloudProfilesApi#updateCloudProfileUsingPUT");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| id |
 **correlationId** | **String**| Correlation ID |
 **requestPayload** | [**CloudProfileRequest**](CloudProfileRequest.md)| Parameters that define a cloud profile | [optional]

### Return type

[**CloudProfileListRepresentation**](CloudProfileListRepresentation.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

