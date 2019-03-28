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

import io.swagger.userManagement.*;
import io.swagger.userManagement.auth.*;
import io.swagger.userManagement.*;
import io.swagger.userManagement.CloudProfilesApi;

import java.io.File;
import java.util.*;

public class CloudProfilesApiExample {

    public static void main(String[] args) {
        
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
    }
}

```

## Documentation for API Endpoints

All URIs are relative to *https://ignitesrv5:30004*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*CloudProfilesApi* | [**addCloudProfileUsingPOST**](docs/CloudProfilesApi.md#addCloudProfileUsingPOST) | **POST** /v1/users/cloudprofile | Add a new cloud profile
*CloudProfilesApi* | [**deleteCloudProfileUsingDELETE**](docs/CloudProfilesApi.md#deleteCloudProfileUsingDELETE) | **DELETE** /v1/users/cloudprofile/{id} | Delete a cloud profile
*CloudProfilesApi* | [**editCloudProfileUsingPATCH**](docs/CloudProfilesApi.md#editCloudProfileUsingPATCH) | **PATCH** /v1/users/cloudprofile/{id} | Edit a cloud profile
*CloudProfilesApi* | [**getCloudProfileUsingGET**](docs/CloudProfilesApi.md#getCloudProfileUsingGET) | **GET** /v1/users/cloudprofile/{userId}/{profileName} | Get cloud profile by business key
*CloudProfilesApi* | [**getCloudProfilesUsingGET**](docs/CloudProfilesApi.md#getCloudProfilesUsingGET) | **GET** /v1/users/cloudprofile/{userId} | Get simplified cloud profiles by user id
*CloudProfilesApi* | [**updateCloudProfileUsingPUT**](docs/CloudProfilesApi.md#updateCloudProfileUsingPUT) | **PUT** /v1/users/cloudprofile/{id} | Update a full cloud profile
*EmailVerificationApi* | [**getIsEmailVerifiedUsingGET**](docs/EmailVerificationApi.md#getIsEmailVerifiedUsingGET) | **GET** /v1/emailVerification/{userId}/isEmailVerified | Get if user email was verified by user id
*EmailVerificationApi* | [**resendEmailVerificationUsingPUT**](docs/EmailVerificationApi.md#resendEmailVerificationUsingPUT) | **PUT** /v1/emailVerification/{userId}/resendEmailVerification | Resend email verification
*EmailVerificationApi* | [**verifyEmailUsingGET**](docs/EmailVerificationApi.md#verifyEmailUsingGET) | **GET** /v1/emailVerification/{token} | Verify user&#39;s email
*UsersApi* | [**addFederatedUserUsingPOST**](docs/UsersApi.md#addFederatedUserUsingPOST) | **POST** /v1/users/federated | Add a new federated user
*UsersApi* | [**addUserUsingPOST**](docs/UsersApi.md#addUserUsingPOST) | **POST** /v1/users | Add a new user
*UsersApi* | [**associateUserToDeviceUsingPATCH**](docs/UsersApi.md#associateUserToDeviceUsingPATCH) | **PATCH** /v1/users/{id}/associateDevice | Associate user to device
*UsersApi* | [**changeUserPasswordUsingPATCH**](docs/UsersApi.md#changeUserPasswordUsingPATCH) | **PATCH** /v1/users/{id}/password | Change user password
*UsersApi* | [**deleteUserUsingDELETE**](docs/UsersApi.md#deleteUserUsingDELETE) | **DELETE** /v1/users/{id} | Delete a user
*UsersApi* | [**deleteUsersByFilterUsingDELETE**](docs/UsersApi.md#deleteUsersByFilterUsingDELETE) | **DELETE** /v1/users | Delete users that match defined criteria
*UsersApi* | [**disassociateDeviceFromUserUsingPATCH**](docs/UsersApi.md#disassociateDeviceFromUserUsingPATCH) | **PATCH** /v1/users/{id}/disassociateDevice | Disassociate a device from a user
*UsersApi* | [**editUserUsingPATCH**](docs/UsersApi.md#editUserUsingPATCH) | **PATCH** /v1/users/{id} | Update a user
*UsersApi* | [**getUserUsingGET**](docs/UsersApi.md#getUserUsingGET) | **GET** /v1/users/{id} | Get a user
*UsersApi* | [**getUsersUsingPOST**](docs/UsersApi.md#getUsersUsingPOST) | **POST** /v1/users/filter | Retrieve users that match defined criteria
*UsersApi* | [**validatePasswordUsingPOST**](docs/UsersApi.md#validatePasswordUsingPOST) | **POST** /v1/passwords/validate | Validate user password


## Documentation for Models

 - [AssociateRequest](docs/AssociateRequest.md)
 - [BaseRepresentation](docs/BaseRepresentation.md)
 - [CloudProfile](docs/CloudProfile.md)
 - [CloudProfileListRepresentation](docs/CloudProfileListRepresentation.md)
 - [CloudProfilePatch](docs/CloudProfilePatch.md)
 - [CloudProfileRequest](docs/CloudProfileRequest.md)
 - [DisassociateDeviceRequest](docs/DisassociateDeviceRequest.md)
 - [EmailVerification](docs/EmailVerification.md)
 - [EmailVerificationRepresentation](docs/EmailVerificationRepresentation.md)
 - [FederatedUserPost](docs/FederatedUserPost.md)
 - [MetadataRepresentation](docs/MetadataRepresentation.md)
 - [PasswordValidationPost](docs/PasswordValidationPost.md)
 - [PasswordValidationRepresentation](docs/PasswordValidationRepresentation.md)
 - [ResponseMessage](docs/ResponseMessage.md)
 - [User](docs/User.md)
 - [UserChangePasswordPatch](docs/UserChangePasswordPatch.md)
 - [UserPatch](docs/UserPatch.md)
 - [UserPost](docs/UserPost.md)
 - [UserRepresentation](docs/UserRepresentation.md)
 - [UsersDeleteFilter](docs/UsersDeleteFilter.md)
 - [UsersGetFilter](docs/UsersGetFilter.md)
 - [UsersListRepresentation](docs/UsersListRepresentation.md)


## Documentation for Authorization

All endpoints do not require authorization.
Authentication schemes defined for the API:

## Recommendation

It's recommended to create an instance of `ApiClient` per thread in a multithreaded environment to avoid any potential issues.

## Author



