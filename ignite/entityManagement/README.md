# swagger-java-client

## Requirements

Building the API client library requires [Maven](https://maven.apache.org/) to be installed.

## Installation

To install the API client library to your local Maven repository, simply execute:

```shell
mvn install
```

To deploy it to a remote Maven repository instead, configure the settings of the repository and execute:

```shell
mvn deploy
```

Refer to the [official documentation](https://maven.apache.org/plugins/maven-deploy-plugin/usage.html) for more information.

### Maven users

Add this dependency to your project's POM:

```xml
<dependency>
    <groupId>io.swagger</groupId>
    <artifactId>swagger-java-client</artifactId>
    <version>1.0.0</version>
    <scope>compile</scope>
</dependency>
```

### Gradle users

Add this dependency to your project's build file:

```groovy
compile "io.swagger:swagger-java-client:1.0.0"
```

### Others

At first generate the JAR by executing:

    mvn package

Then manually install the following JARs:

* target/swagger-java-client-1.0.0.jar
* target/lib/*.jar

## Getting Started

Please follow the [installation](#installation) instruction and execute the following Java code:

```java

import io.swagger.entityManagement.*;
import io.swagger.entityManagement.auth.*;
import io.swagger.entityManagement.*;
import io.swagger.entityManagement.EntityProcessApi;

import java.io.File;
import java.util.*;

public class EntityProcessApiExample {

    public static void main(String[] args) {
        
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
    }
}

```

## Documentation for API Endpoints

All URIs are relative to *https://harmanx2.ignite.harmandev.com:8083*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*EntityProcessApi* | [**addEntityAttributesUsingPUT**](docs/EntityProcessApi.md#addEntityAttributesUsingPUT) | **PUT** /v1/metadata/attributes/{entityName} | Add additional attributes to an entity
*EntityProcessApi* | [**addEntityUsingPOST**](docs/EntityProcessApi.md#addEntityUsingPOST) | **POST** /v1/entities/{entityName} | Add a new entity
*EntityProcessApi* | [**addMetaDataUsingPOST**](docs/EntityProcessApi.md#addMetaDataUsingPOST) | **POST** /v1/metadata | addMetaData
*EntityProcessApi* | [**deleteEntitiesUsingDELETE**](docs/EntityProcessApi.md#deleteEntitiesUsingDELETE) | **DELETE** /v1/entities/{entityName} | Delete entities by filter
*EntityProcessApi* | [**deleteEntityUsingDELETE**](docs/EntityProcessApi.md#deleteEntityUsingDELETE) | **DELETE** /v1/entities/{entityName}/{ids} | Delete an entity
*EntityProcessApi* | [**deleteMetadataUsingDELETE**](docs/EntityProcessApi.md#deleteMetadataUsingDELETE) | **DELETE** /v1/metadata/{entityName} | Delete metadata
*EntityProcessApi* | [**editEntityUsingPATCH**](docs/EntityProcessApi.md#editEntityUsingPATCH) | **PATCH** /v1/entities/{entityName}/{id} | Update an entity
*EntityProcessApi* | [**editEntityUsingPUT**](docs/EntityProcessApi.md#editEntityUsingPUT) | **PUT** /v1/entities/{entityName}/{id} | Update an entity
*EntityProcessApi* | [**getAllEntitiesMetadataUsingGET**](docs/EntityProcessApi.md#getAllEntitiesMetadataUsingGET) | **GET** /v1/metadata | getAllEntitiesMetadata
*EntityProcessApi* | [**getEntitiesByFilterUsingPOST**](docs/EntityProcessApi.md#getEntitiesByFilterUsingPOST) | **POST** /v1/entities/{entityName}/filter | Filter entities
*EntityProcessApi* | [**getEntitiesMetadataUsingGET**](docs/EntityProcessApi.md#getEntitiesMetadataUsingGET) | **GET** /v1/metadata/{entityName} | Get entity metadata
*EntityProcessApi* | [**getEntitiesUsingGET**](docs/EntityProcessApi.md#getEntitiesUsingGET) | **GET** /v1/entities/{entityName} | Get all entities from a schema
*EntityProcessApi* | [**getEntityUsingGET**](docs/EntityProcessApi.md#getEntityUsingGET) | **GET** /v1/entities/{entityName}/{id} | Get entity


## Documentation for Models

 - [CollectionEntityMetaData](docs/CollectionEntityMetaData.md)
 - [EntityMetaData](docs/EntityMetaData.md)
 - [FieldMetaData](docs/FieldMetaData.md)
 - [ObjectNode](docs/ObjectNode.md)
 - [Pattern](docs/Pattern.md)


## Documentation for Authorization

All endpoints do not require authorization.
Authentication schemes defined for the API:

## Recommendation

It's recommended to create an instance of `ApiClient` per thread in a multithreaded environment to avoid any potential issues.

## Author



