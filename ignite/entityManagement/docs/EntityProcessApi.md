# EntityProcessApi

All URIs are relative to *https://harmanx2.ignite.harmandev.com:8083*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addEntityAttributesUsingPUT**](EntityProcessApi.md#addEntityAttributesUsingPUT) | **PUT** /v1/metadata/attributes/{entityName} | Add additional attributes to an entity
[**addEntityUsingPOST**](EntityProcessApi.md#addEntityUsingPOST) | **POST** /v1/entities/{entityName} | Add a new entity
[**addMetaDataUsingPOST**](EntityProcessApi.md#addMetaDataUsingPOST) | **POST** /v1/metadata | addMetaData
[**deleteEntitiesUsingDELETE**](EntityProcessApi.md#deleteEntitiesUsingDELETE) | **DELETE** /v1/entities/{entityName} | Delete entities by filter
[**deleteEntityUsingDELETE**](EntityProcessApi.md#deleteEntityUsingDELETE) | **DELETE** /v1/entities/{entityName}/{ids} | Delete an entity
[**deleteMetadataUsingDELETE**](EntityProcessApi.md#deleteMetadataUsingDELETE) | **DELETE** /v1/metadata/{entityName} | Delete metadata
[**editEntityUsingPATCH**](EntityProcessApi.md#editEntityUsingPATCH) | **PATCH** /v1/entities/{entityName}/{id} | Update an entity
[**editEntityUsingPUT**](EntityProcessApi.md#editEntityUsingPUT) | **PUT** /v1/entities/{entityName}/{id} | Update an entity
[**getAllEntitiesMetadataUsingGET**](EntityProcessApi.md#getAllEntitiesMetadataUsingGET) | **GET** /v1/metadata | getAllEntitiesMetadata
[**getEntitiesByFilterUsingPOST**](EntityProcessApi.md#getEntitiesByFilterUsingPOST) | **POST** /v1/entities/{entityName}/filter | Filter entities
[**getEntitiesMetadataUsingGET**](EntityProcessApi.md#getEntitiesMetadataUsingGET) | **GET** /v1/metadata/{entityName} | Get entity metadata
[**getEntitiesUsingGET**](EntityProcessApi.md#getEntitiesUsingGET) | **GET** /v1/entities/{entityName} | Get all entities from a schema
[**getEntityUsingGET**](EntityProcessApi.md#getEntityUsingGET) | **GET** /v1/entities/{entityName}/{id} | Get entity


<a name="addEntityAttributesUsingPUT"></a>
# **addEntityAttributesUsingPUT**
> Map&lt;String, Object&gt; addEntityAttributesUsingPUT(correlationId, entityName, requestPayload)

Add additional attributes to an entity

Add additional attributes to a given entity.     Each attribute is defined by set of metadata fields described below:      ** name ** - May contain underscore and alphanumeric characters. This field is mandatory and case sensitive     ** mandatory ** - Field value is mandatory when adding or updating    ** unique ** - There cannot be two equal values    ** readOnly ** - The value cannot be modified after its added    ** searchable ** - Allow this field to be part of a filter when performing get request    ** type ** - Allowed types: TEXT, NUMBER, LONG_NUMBER, JSON, DATE    ** regex ** - Field validation regex 

### Example
```java
// Import classes:
//import io.swagger.entityManagement.ApiException;
//import io.swagger.entityManagement.api.EntityProcessApi;


EntityProcessApi apiInstance = new EntityProcessApi();
String correlationId = "correlationId_example"; // String | Correlation ID
String entityName = "entityName_example"; // String | entityName
List<FieldMetaData> requestPayload = Arrays.asList(new FieldMetaData()); // List<FieldMetaData> | Attributes
try {
    Map<String, Object> result = apiInstance.addEntityAttributesUsingPUT(correlationId, entityName, requestPayload);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EntityProcessApi#addEntityAttributesUsingPUT");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **correlationId** | **String**| Correlation ID |
 **entityName** | **String**| entityName |
 **requestPayload** | [**List&lt;FieldMetaData&gt;**](FieldMetaData.md)| Attributes | [optional]

### Return type

**Map&lt;String, Object&gt;**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="addEntityUsingPOST"></a>
# **addEntityUsingPOST**
> Map&lt;String, Object&gt; addEntityUsingPOST(correlationId, entityName, requestPayload, source, refresh)

Add a new entity

Adds a new entity to any of the microservices schemas. The schema name must be specified (entityName)

### Example
```java
// Import classes:
//import io.swagger.entityManagement.ApiException;
//import io.swagger.entityManagement.api.EntityProcessApi;


EntityProcessApi apiInstance = new EntityProcessApi();
String correlationId = "correlationId_example"; // String | Correlation ID
String entityName = "entityName_example"; // String | Schema name
Object requestPayload = null; // Object | the payload must correspond to the target schema, please open the relevant microservice documentation for the relevant data
Boolean source = true; // Boolean | boolean, if true - retrieves the entity after it is committed to be saved
Boolean refresh = true; // Boolean | boolean, false - bulk save of new entities, if true - force save of the new entity to the hard drive
try {
    Map<String, Object> result = apiInstance.addEntityUsingPOST(correlationId, entityName, requestPayload, source, refresh);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EntityProcessApi#addEntityUsingPOST");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **correlationId** | **String**| Correlation ID |
 **entityName** | **String**| Schema name |
 **requestPayload** | **Object**| the payload must correspond to the target schema, please open the relevant microservice documentation for the relevant data | [optional]
 **source** | **Boolean**| boolean, if true - retrieves the entity after it is committed to be saved | [optional]
 **refresh** | **Boolean**| boolean, false - bulk save of new entities, if true - force save of the new entity to the hard drive | [optional]

### Return type

**Map&lt;String, Object&gt;**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="addMetaDataUsingPOST"></a>
# **addMetaDataUsingPOST**
> Map&lt;String, Object&gt; addMetaDataUsingPOST(correlationId, entityMetaData)

addMetaData

### Example
```java
// Import classes:
//import io.swagger.entityManagement.ApiException;
//import io.swagger.entityManagement.api.EntityProcessApi;


EntityProcessApi apiInstance = new EntityProcessApi();
String correlationId = "correlationId_example"; // String | Correlation ID
EntityMetaData entityMetaData = new EntityMetaData(); // EntityMetaData | entityMetaData
try {
    Map<String, Object> result = apiInstance.addMetaDataUsingPOST(correlationId, entityMetaData);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EntityProcessApi#addMetaDataUsingPOST");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **correlationId** | **String**| Correlation ID |
 **entityMetaData** | [**EntityMetaData**](EntityMetaData.md)| entityMetaData | [optional]

### Return type

**Map&lt;String, Object&gt;**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="deleteEntitiesUsingDELETE"></a>
# **deleteEntitiesUsingDELETE**
> Object deleteEntitiesUsingDELETE(correlationId, entityName, refresh, requestPayload)

Delete entities by filter

### Example
```java
// Import classes:
//import io.swagger.entityManagement.ApiException;
//import io.swagger.entityManagement.api.EntityProcessApi;


EntityProcessApi apiInstance = new EntityProcessApi();
String correlationId = "correlationId_example"; // String | Correlation ID
String entityName = "entityName_example"; // String | Schema name
Boolean refresh = true; // Boolean | boolean, if true - force delete of the entity from hard drive
Object requestPayload = null; // Object | jsonNodes
try {
    Object result = apiInstance.deleteEntitiesUsingDELETE(correlationId, entityName, refresh, requestPayload);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EntityProcessApi#deleteEntitiesUsingDELETE");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **correlationId** | **String**| Correlation ID |
 **entityName** | **String**| Schema name |
 **refresh** | **Boolean**| boolean, if true - force delete of the entity from hard drive | [optional]
 **requestPayload** | **Object**| jsonNodes | [optional]

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="deleteEntityUsingDELETE"></a>
# **deleteEntityUsingDELETE**
> Object deleteEntityUsingDELETE(ids, correlationId, entityName, refresh)

Delete an entity

### Example
```java
// Import classes:
//import io.swagger.entityManagement.ApiException;
//import io.swagger.entityManagement.api.EntityProcessApi;


EntityProcessApi apiInstance = new EntityProcessApi();
String ids = "ids_example"; // String | ids
String correlationId = "correlationId_example"; // String | Correlation ID
String entityName = "entityName_example"; // String | Schema name
Boolean refresh = true; // Boolean | boolean, if true - force delete of the entity from hard drive
try {
    Object result = apiInstance.deleteEntityUsingDELETE(ids, correlationId, entityName, refresh);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EntityProcessApi#deleteEntityUsingDELETE");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ids** | **String**| ids |
 **correlationId** | **String**| Correlation ID |
 **entityName** | **String**| Schema name |
 **refresh** | **Boolean**| boolean, if true - force delete of the entity from hard drive | [optional]

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="deleteMetadataUsingDELETE"></a>
# **deleteMetadataUsingDELETE**
> Object deleteMetadataUsingDELETE(correlationId, entityName)

Delete metadata

### Example
```java
// Import classes:
//import io.swagger.entityManagement.ApiException;
//import io.swagger.entityManagement.api.EntityProcessApi;


EntityProcessApi apiInstance = new EntityProcessApi();
String correlationId = "correlationId_example"; // String | Correlation ID
String entityName = "entityName_example"; // String | Metadata name
try {
    Object result = apiInstance.deleteMetadataUsingDELETE(correlationId, entityName);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EntityProcessApi#deleteMetadataUsingDELETE");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **correlationId** | **String**| Correlation ID |
 **entityName** | **String**| Metadata name |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="editEntityUsingPATCH"></a>
# **editEntityUsingPATCH**
> Map&lt;String, Object&gt; editEntityUsingPATCH(id, entityBody, correlationId, entityName, source, refresh)

Update an entity

Updates a single entity

### Example
```java
// Import classes:
//import io.swagger.entityManagement.ApiException;
//import io.swagger.entityManagement.api.EntityProcessApi;


EntityProcessApi apiInstance = new EntityProcessApi();
String id = "id_example"; // String | Entity ID
Object entityBody = null; // Object | entityBody
String correlationId = "correlationId_example"; // String | Correlation ID
String entityName = "entityName_example"; // String | Schema name
Boolean source = true; // Boolean | source
Boolean refresh = true; // Boolean | refresh
try {
    Map<String, Object> result = apiInstance.editEntityUsingPATCH(id, entityBody, correlationId, entityName, source, refresh);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EntityProcessApi#editEntityUsingPATCH");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| Entity ID |
 **entityBody** | **Object**| entityBody |
 **correlationId** | **String**| Correlation ID |
 **entityName** | **String**| Schema name |
 **source** | **Boolean**| source | [optional]
 **refresh** | **Boolean**| refresh | [optional]

### Return type

**Map&lt;String, Object&gt;**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="editEntityUsingPUT"></a>
# **editEntityUsingPUT**
> Map&lt;String, Object&gt; editEntityUsingPUT(id, entityBody, correlationId, entityName, source, refresh)

Update an entity

Updates a single entity

### Example
```java
// Import classes:
//import io.swagger.entityManagement.ApiException;
//import io.swagger.entityManagement.api.EntityProcessApi;


EntityProcessApi apiInstance = new EntityProcessApi();
String id = "id_example"; // String | Entity ID
Object entityBody = null; // Object | entityBody
String correlationId = "correlationId_example"; // String | Correlation ID
String entityName = "entityName_example"; // String | Schema name
Boolean source = true; // Boolean | source
Boolean refresh = true; // Boolean | refresh
try {
    Map<String, Object> result = apiInstance.editEntityUsingPUT(id, entityBody, correlationId, entityName, source, refresh);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EntityProcessApi#editEntityUsingPUT");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| Entity ID |
 **entityBody** | **Object**| entityBody |
 **correlationId** | **String**| Correlation ID |
 **entityName** | **String**| Schema name |
 **source** | **Boolean**| source | [optional]
 **refresh** | **Boolean**| refresh | [optional]

### Return type

**Map&lt;String, Object&gt;**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getAllEntitiesMetadataUsingGET"></a>
# **getAllEntitiesMetadataUsingGET**
> CollectionEntityMetaData getAllEntitiesMetadataUsingGET(correlationId)

getAllEntitiesMetadata

### Example
```java
// Import classes:
//import io.swagger.entityManagement.ApiException;
//import io.swagger.entityManagement.api.EntityProcessApi;


EntityProcessApi apiInstance = new EntityProcessApi();
String correlationId = "correlationId_example"; // String | Correlation ID
try {
    CollectionEntityMetaData result = apiInstance.getAllEntitiesMetadataUsingGET(correlationId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EntityProcessApi#getAllEntitiesMetadataUsingGET");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **correlationId** | **String**| Correlation ID |

### Return type

[**CollectionEntityMetaData**](CollectionEntityMetaData.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getEntitiesByFilterUsingPOST"></a>
# **getEntitiesByFilterUsingPOST**
> Map&lt;String, Object&gt; getEntitiesByFilterUsingPOST(correlationId, entityName, jsonNodes, from, size, sortBy, sortOrder)

Filter entities

Filter entities from a specific schema by one or more parameters.To get all entities, an empty body can be used.

### Example
```java
// Import classes:
//import io.swagger.entityManagement.ApiException;
//import io.swagger.entityManagement.api.EntityProcessApi;


EntityProcessApi apiInstance = new EntityProcessApi();
String correlationId = "correlationId_example"; // String | Correlation ID
String entityName = "entityName_example"; // String | Schema name
Object jsonNodes = null; // Object | jsonNodes
Integer from = 56; // Integer | 
Integer size = 56; // Integer | 
String sortBy = "sortBy_example"; // String | 
String sortOrder = "sortOrder_example"; // String | 
try {
    Map<String, Object> result = apiInstance.getEntitiesByFilterUsingPOST(correlationId, entityName, jsonNodes, from, size, sortBy, sortOrder);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EntityProcessApi#getEntitiesByFilterUsingPOST");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **correlationId** | **String**| Correlation ID |
 **entityName** | **String**| Schema name |
 **jsonNodes** | **Object**| jsonNodes | [optional]
 **from** | **Integer**|  | [optional]
 **size** | **Integer**|  | [optional]
 **sortBy** | **String**|  | [optional]
 **sortOrder** | **String**|  | [optional]

### Return type

**Map&lt;String, Object&gt;**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getEntitiesMetadataUsingGET"></a>
# **getEntitiesMetadataUsingGET**
> EntityMetaData getEntitiesMetadataUsingGET(correlationId, entityName)

Get entity metadata

Get metadata of an entity. Metadata fields described below:    ** name ** - May contain underscore and alphanumeric characters. This field is mandatory and case sensitive     ** mandatory ** - Field value is mandatory when adding or updating    ** unique ** - There cannot be two equal values    ** readOnly ** - The value cannot be modified after its added    ** searchable ** - Allow this field to be part of a filter when performing get request    ** type ** - Allowed types: TEXT, NUMBER, LONG_NUMBER, JSON, DATE    ** regex ** - Field validation regex      **dynamicAttribute ** - Informs if the field was dynamically inserted 

### Example
```java
// Import classes:
//import io.swagger.entityManagement.ApiException;
//import io.swagger.entityManagement.api.EntityProcessApi;


EntityProcessApi apiInstance = new EntityProcessApi();
String correlationId = "correlationId_example"; // String | Correlation ID
String entityName = "entityName_example"; // String | Metadata name
try {
    EntityMetaData result = apiInstance.getEntitiesMetadataUsingGET(correlationId, entityName);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EntityProcessApi#getEntitiesMetadataUsingGET");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **correlationId** | **String**| Correlation ID |
 **entityName** | **String**| Metadata name |

### Return type

[**EntityMetaData**](EntityMetaData.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getEntitiesUsingGET"></a>
# **getEntitiesUsingGET**
> Map&lt;String, Object&gt; getEntitiesUsingGET(correlationId, entityName, from, size, sortBy, sortOrder)

Get all entities from a schema

Get all entities from a specific schema.

### Example
```java
// Import classes:
//import io.swagger.entityManagement.ApiException;
//import io.swagger.entityManagement.api.EntityProcessApi;


EntityProcessApi apiInstance = new EntityProcessApi();
String correlationId = "correlationId_example"; // String | Correlation ID
String entityName = "entityName_example"; // String | Schema name
Object from = null; // Object | 
Object size = null; // Object | 
String sortBy = "sortBy_example"; // String | 
String sortOrder = "sortOrder_example"; // String | 
try {
    Map<String, Object> result = apiInstance.getEntitiesUsingGET(correlationId, entityName, from, size, sortBy, sortOrder);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EntityProcessApi#getEntitiesUsingGET");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **correlationId** | **String**| Correlation ID |
 **entityName** | **String**| Schema name |
 **from** | [**Object**](.md)|  | [optional]
 **size** | [**Object**](.md)|  | [optional]
 **sortBy** | **String**|  | [optional]
 **sortOrder** | **String**|  | [optional]

### Return type

**Map&lt;String, Object&gt;**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getEntityUsingGET"></a>
# **getEntityUsingGET**
> Map&lt;String, Object&gt; getEntityUsingGET(id, correlationId, entityName)

Get entity

Get a single entity by its ID

### Example
```java
// Import classes:
//import io.swagger.entityManagement.ApiException;
//import io.swagger.entityManagement.api.EntityProcessApi;


EntityProcessApi apiInstance = new EntityProcessApi();
String id = "id_example"; // String | id
String correlationId = "correlationId_example"; // String | Correlation ID
String entityName = "entityName_example"; // String | Schema name
try {
    Map<String, Object> result = apiInstance.getEntityUsingGET(id, correlationId, entityName);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EntityProcessApi#getEntityUsingGET");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| id |
 **correlationId** | **String**| Correlation ID |
 **entityName** | **String**| Schema name |

### Return type

**Map&lt;String, Object&gt;**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

