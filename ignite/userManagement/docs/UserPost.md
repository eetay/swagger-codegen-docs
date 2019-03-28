
# UserPost

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**address1** | **String** | Address. Maximum length &#x3D; 50 chars |  [optional]
**address2** | **String** | Address. Maximum length &#x3D; 100 chars |  [optional]
**birthDate** | [**LocalDate**](LocalDate.md) | Birth Date in ISO 8601 format (yyyy-MM-dd) |  [optional]
**city** | **String** | City. Maximum length &#x3D; 50 chars |  [optional]
**country** | **String** | Country. Maximum length &#x3D; 50 chars |  [optional]
**email** | **String** | Email address. Minimum length &#x3D; 3, Maximum length &#x3D; 128 chars |  [optional]
**firstName** | **String** | First name. Maximum length &#x3D; 49 chars |  [optional]
**gender** | [**GenderEnum**](#GenderEnum) | Gender |  [optional]
**lastName** | **String** | Last name. Maximum length &#x3D; 49 chars |  [optional]
**locale** | **String** | Locale. Maximum length &#x3D; 5 chars |  [optional]
**password** | **String** |    User password. Password length should be between 6 to 80 chars and must use at least three of the four available character types: lowercase letters, uppercase letters, numbers, and any character from the following list:     ** &amp;#124;#$%&amp;&#39;()*+,-./:;&lt;&#x3D;&gt;?@[]^_&#x60;{}~ ** | 
**phoneNumber** | **String** | Phone number. Minimum length &#x3D; 5, Maximum length &#x3D; 16 chars |  [optional]
**postalCode** | **String** | Postal Code. Maximum length &#x3D; 11 chars |  [optional]
**role** | **String** | Role. Allowed values are: [VEHICLE_OWNER, OEM_ADMIN, BUSINESS_ADMIN] or one of the defined custom roles | 
**state** | **String** | State. Maximum length &#x3D; 50 chars |  [optional]
**userName** | **String** | Username. Maximum length &#x3D; 254 chars | 


<a name="GenderEnum"></a>
## Enum: GenderEnum
Name | Value
---- | -----
MALE | &quot;MALE&quot;
FEMALE | &quot;FEMALE&quot;



