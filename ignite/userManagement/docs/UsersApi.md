# UsersApi

All URIs are relative to *https://ignitesrv5:30004*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addFederatedUserUsingPOST**](UsersApi.md#addFederatedUserUsingPOST) | **POST** /v1/users/federated | Add a new federated user
[**addUserUsingPOST**](UsersApi.md#addUserUsingPOST) | **POST** /v1/users | Add a new user
[**associateUserToDeviceUsingPATCH**](UsersApi.md#associateUserToDeviceUsingPATCH) | **PATCH** /v1/users/{id}/associateDevice | Associate user to device
[**changeUserPasswordUsingPATCH**](UsersApi.md#changeUserPasswordUsingPATCH) | **PATCH** /v1/users/{id}/password | Change user password
[**deleteUserUsingDELETE**](UsersApi.md#deleteUserUsingDELETE) | **DELETE** /v1/users/{id} | Delete a user
[**deleteUsersByFilterUsingDELETE**](UsersApi.md#deleteUsersByFilterUsingDELETE) | **DELETE** /v1/users | Delete users that match defined criteria
[**disassociateDeviceFromUserUsingPATCH**](UsersApi.md#disassociateDeviceFromUserUsingPATCH) | **PATCH** /v1/users/{id}/disassociateDevice | Disassociate a device from a user
[**editUserUsingPATCH**](UsersApi.md#editUserUsingPATCH) | **PATCH** /v1/users/{id} | Update a user
[**getUserUsingGET**](UsersApi.md#getUserUsingGET) | **GET** /v1/users/{id} | Get a user
[**getUsersUsingPOST**](UsersApi.md#getUsersUsingPOST) | **POST** /v1/users/filter | Retrieve users that match defined criteria
[**validatePasswordUsingPOST**](UsersApi.md#validatePasswordUsingPOST) | **POST** /v1/passwords/validate | Validate user password


<a name="addFederatedUserUsingPOST"></a>
# **addFederatedUserUsingPOST**
> UserRepresentation addFederatedUserUsingPOST(correlationId, session, requestPayload)

Add a new federated user

Creates a new federated user.   

### Example
```java
// Import classes:
//import io.swagger.userManagement.ApiException;
//import io.swagger.userManagement.api.UsersApi;


UsersApi apiInstance = new UsersApi();
String correlationId = "correlationId_example"; // String | Correlation ID
Object session = null; // Object | session
FederatedUserPost requestPayload = new FederatedUserPost(); // FederatedUserPost | Parameters that define a single federated user
try {
    UserRepresentation result = apiInstance.addFederatedUserUsingPOST(correlationId, session, requestPayload);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UsersApi#addFederatedUserUsingPOST");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **correlationId** | **String**| Correlation ID |
 **session** | [**Object**](.md)| session | [optional]
 **requestPayload** | [**FederatedUserPost**](FederatedUserPost.md)| Parameters that define a single federated user | [optional]

### Return type

[**UserRepresentation**](UserRepresentation.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="addUserUsingPOST"></a>
# **addUserUsingPOST**
> UserRepresentation addUserUsingPOST(session, correlationId, requestPayload)

Add a new user

Creates a new user.   

### Example
```java
// Import classes:
//import io.swagger.userManagement.ApiException;
//import io.swagger.userManagement.api.UsersApi;


UsersApi apiInstance = new UsersApi();
Object session = null; // Object | session
String correlationId = "correlationId_example"; // String | Correlation ID
UserPost requestPayload = new UserPost(); // UserPost | Parameters that define a single user
try {
    UserRepresentation result = apiInstance.addUserUsingPOST(session, correlationId, requestPayload);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UsersApi#addUserUsingPOST");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **session** | [**Object**](.md)| session |
 **correlationId** | **String**| Correlation ID |
 **requestPayload** | [**UserPost**](UserPost.md)| Parameters that define a single user | [optional]

### Return type

[**UserRepresentation**](UserRepresentation.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="associateUserToDeviceUsingPATCH"></a>
# **associateUserToDeviceUsingPATCH**
> UserRepresentation associateUserToDeviceUsingPATCH(session, id, correlationId, requestPayload)

Associate user to device

Associate user to device that is identified by a token.

### Example
```java
// Import classes:
//import io.swagger.userManagement.ApiException;
//import io.swagger.userManagement.api.UsersApi;


UsersApi apiInstance = new UsersApi();
Object session = null; // Object | session
String id = "id_example"; // String | User ID
String correlationId = "correlationId_example"; // String | Correlation ID
AssociateRequest requestPayload = new AssociateRequest(); // AssociateRequest | Device token that will be used to identify the device
try {
    UserRepresentation result = apiInstance.associateUserToDeviceUsingPATCH(session, id, correlationId, requestPayload);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UsersApi#associateUserToDeviceUsingPATCH");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **session** | [**Object**](.md)| session |
 **id** | **String**| User ID |
 **correlationId** | **String**| Correlation ID |
 **requestPayload** | [**AssociateRequest**](AssociateRequest.md)| Device token that will be used to identify the device | [optional]

### Return type

[**UserRepresentation**](UserRepresentation.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="changeUserPasswordUsingPATCH"></a>
# **changeUserPasswordUsingPATCH**
> UserRepresentation changeUserPasswordUsingPATCH(session, id, correlationId, requestPayload)

Change user password

Change the password for a single user

### Example
```java
// Import classes:
//import io.swagger.userManagement.ApiException;
//import io.swagger.userManagement.api.UsersApi;


UsersApi apiInstance = new UsersApi();
Object session = null; // Object | session
String id = "id_example"; // String | User ID
String correlationId = "correlationId_example"; // String | Correlation ID
UserChangePasswordPatch requestPayload = new UserChangePasswordPatch(); // UserChangePasswordPatch | Parameters that update a single user password
try {
    UserRepresentation result = apiInstance.changeUserPasswordUsingPATCH(session, id, correlationId, requestPayload);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UsersApi#changeUserPasswordUsingPATCH");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **session** | [**Object**](.md)| session |
 **id** | **String**| User ID |
 **correlationId** | **String**| Correlation ID |
 **requestPayload** | [**UserChangePasswordPatch**](UserChangePasswordPatch.md)| Parameters that update a single user password | [optional]

### Return type

[**UserRepresentation**](UserRepresentation.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="deleteUserUsingDELETE"></a>
# **deleteUserUsingDELETE**
> BaseRepresentation deleteUserUsingDELETE(session, id, correlationId)

Delete a user

Deletes a single user identified by its ID

### Example
```java
// Import classes:
//import io.swagger.userManagement.ApiException;
//import io.swagger.userManagement.api.UsersApi;


UsersApi apiInstance = new UsersApi();
Object session = null; // Object | session
String id = "id_example"; // String | User ID
String correlationId = "correlationId_example"; // String | Correlation ID
try {
    BaseRepresentation result = apiInstance.deleteUserUsingDELETE(session, id, correlationId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UsersApi#deleteUserUsingDELETE");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **session** | [**Object**](.md)| session |
 **id** | **String**| User ID |
 **correlationId** | **String**| Correlation ID |

### Return type

[**BaseRepresentation**](BaseRepresentation.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="deleteUsersByFilterUsingDELETE"></a>
# **deleteUsersByFilterUsingDELETE**
> BaseRepresentation deleteUsersByFilterUsingDELETE(session, correlationId, requestPayload)

Delete users that match defined criteria

Deletes users that match items in the list of defined parameters and values

### Example
```java
// Import classes:
//import io.swagger.userManagement.ApiException;
//import io.swagger.userManagement.api.UsersApi;


UsersApi apiInstance = new UsersApi();
Object session = null; // Object | session
String correlationId = "correlationId_example"; // String | Correlation ID
UsersDeleteFilter requestPayload = new UsersDeleteFilter(); // UsersDeleteFilter | List of user parameters and values
try {
    BaseRepresentation result = apiInstance.deleteUsersByFilterUsingDELETE(session, correlationId, requestPayload);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UsersApi#deleteUsersByFilterUsingDELETE");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **session** | [**Object**](.md)| session |
 **correlationId** | **String**| Correlation ID |
 **requestPayload** | [**UsersDeleteFilter**](UsersDeleteFilter.md)| List of user parameters and values | [optional]

### Return type

[**BaseRepresentation**](BaseRepresentation.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="disassociateDeviceFromUserUsingPATCH"></a>
# **disassociateDeviceFromUserUsingPATCH**
> UserRepresentation disassociateDeviceFromUserUsingPATCH(session, id, correlationId, refresh, requestPayload)

Disassociate a device from a user

Disassociate a device from a user.

### Example
```java
// Import classes:
//import io.swagger.userManagement.ApiException;
//import io.swagger.userManagement.api.UsersApi;


UsersApi apiInstance = new UsersApi();
Object session = null; // Object | session
String id = "id_example"; // String | User ID
String correlationId = "correlationId_example"; // String | Correlation ID
Boolean refresh = true; // Boolean | boolean, false - bulk save of new entities, if true - force save of the new entity to the hard drive
DisassociateDeviceRequest requestPayload = new DisassociateDeviceRequest(); // DisassociateDeviceRequest | Device Id to disassociate
try {
    UserRepresentation result = apiInstance.disassociateDeviceFromUserUsingPATCH(session, id, correlationId, refresh, requestPayload);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UsersApi#disassociateDeviceFromUserUsingPATCH");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **session** | [**Object**](.md)| session |
 **id** | **String**| User ID |
 **correlationId** | **String**| Correlation ID |
 **refresh** | **Boolean**| boolean, false - bulk save of new entities, if true - force save of the new entity to the hard drive | [optional]
 **requestPayload** | [**DisassociateDeviceRequest**](DisassociateDeviceRequest.md)| Device Id to disassociate | [optional]

### Return type

[**UserRepresentation**](UserRepresentation.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="editUserUsingPATCH"></a>
# **editUserUsingPATCH**
> UserRepresentation editUserUsingPATCH(session, id, correlationId, requestPayload)

Update a user

Updates a single user identified by its ID

### Example
```java
// Import classes:
//import io.swagger.userManagement.ApiException;
//import io.swagger.userManagement.api.UsersApi;


UsersApi apiInstance = new UsersApi();
Object session = null; // Object | session
String id = "id_example"; // String | User ID
String correlationId = "correlationId_example"; // String | Correlation ID
UserPatch requestPayload = new UserPatch(); // UserPatch | Parameters that update a single user
try {
    UserRepresentation result = apiInstance.editUserUsingPATCH(session, id, correlationId, requestPayload);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UsersApi#editUserUsingPATCH");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **session** | [**Object**](.md)| session |
 **id** | **String**| User ID |
 **correlationId** | **String**| Correlation ID |
 **requestPayload** | [**UserPatch**](UserPatch.md)| Parameters that update a single user | [optional]

### Return type

[**UserRepresentation**](UserRepresentation.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getUserUsingGET"></a>
# **getUserUsingGET**
> UserRepresentation getUserUsingGET(id, correlationId, session)

Get a user

Gets a single user identified by its ID

### Example
```java
// Import classes:
//import io.swagger.userManagement.ApiException;
//import io.swagger.userManagement.api.UsersApi;


UsersApi apiInstance = new UsersApi();
String id = "id_example"; // String | User ID
String correlationId = "correlationId_example"; // String | Correlation ID
Object session = null; // Object | session
try {
    UserRepresentation result = apiInstance.getUserUsingGET(id, correlationId, session);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UsersApi#getUserUsingGET");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| User ID |
 **correlationId** | **String**| Correlation ID |
 **session** | [**Object**](.md)| session | [optional]

### Return type

[**UserRepresentation**](UserRepresentation.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getUsersUsingPOST"></a>
# **getUsersUsingPOST**
> UsersListRepresentation getUsersUsingPOST(correlationId, pageNumber, pageSize, sortBy, sortOrder, session, requestPayload)

Retrieve users that match defined criteria

&#39;Retrieves users that match items in the defined list of parameters and values.\\n&#39; +   List of parameters can contain dynamic attributes only if they were defined as \\&#39;searchable\\&#39;.

### Example
```java
// Import classes:
//import io.swagger.userManagement.ApiException;
//import io.swagger.userManagement.api.UsersApi;


UsersApi apiInstance = new UsersApi();
String correlationId = "correlationId_example"; // String | Correlation ID
Integer pageNumber = 0; // Integer | Page number to retrieve; the first page is 0
Integer pageSize = 20; // Integer | Number of items to display per page
String sortBy = "sortBy_example"; // String | Parameters to sort by
String sortOrder = "DESC"; // String | Sort in ascending (ASC) or descending (DESC) order; default: descending
Object session = null; // Object | session
UsersGetFilter requestPayload = new UsersGetFilter(); // UsersGetFilter | Parameters and values by which to filter. To get all users, leave empty.
try {
    UsersListRepresentation result = apiInstance.getUsersUsingPOST(correlationId, pageNumber, pageSize, sortBy, sortOrder, session, requestPayload);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UsersApi#getUsersUsingPOST");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **correlationId** | **String**| Correlation ID |
 **pageNumber** | **Integer**| Page number to retrieve; the first page is 0 | [optional] [default to 0]
 **pageSize** | **Integer**| Number of items to display per page | [optional] [default to 20]
 **sortBy** | **String**| Parameters to sort by | [optional] [enum: IDS, USER_NAMES, ROLES, FIRST_NAMES, LAST_NAMES, COUNTRIES, STATES, CITIES, ADDRESS1, ADDRESS2, POSTAL_CODES, PHONE_NUMBERS, EMAILS, GENDER, LOCALES, DEV_IDS]
 **sortOrder** | **String**| Sort in ascending (ASC) or descending (DESC) order; default: descending | [optional] [default to DESC] [enum: DESC, ASC]
 **session** | [**Object**](.md)| session | [optional]
 **requestPayload** | [**UsersGetFilter**](UsersGetFilter.md)| Parameters and values by which to filter. To get all users, leave empty. | [optional]

### Return type

[**UsersListRepresentation**](UsersListRepresentation.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="validatePasswordUsingPOST"></a>
# **validatePasswordUsingPOST**
> PasswordValidationRepresentation validatePasswordUsingPOST(correlationId, requestPayload)

Validate user password

Validates user password.   

### Example
```java
// Import classes:
//import io.swagger.userManagement.ApiException;
//import io.swagger.userManagement.api.UsersApi;


UsersApi apiInstance = new UsersApi();
String correlationId = "correlationId_example"; // String | Correlation ID
PasswordValidationPost requestPayload = new PasswordValidationPost(); // PasswordValidationPost | Parameters that are required to validate user's password
try {
    PasswordValidationRepresentation result = apiInstance.validatePasswordUsingPOST(correlationId, requestPayload);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UsersApi#validatePasswordUsingPOST");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **correlationId** | **String**| Correlation ID |
 **requestPayload** | [**PasswordValidationPost**](PasswordValidationPost.md)| Parameters that are required to validate user&#39;s password | [optional]

### Return type

[**PasswordValidationRepresentation**](PasswordValidationRepresentation.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

