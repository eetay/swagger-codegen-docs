
# FieldMetaData

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**mandatory** | **Boolean** |  |  [optional]
**name** | **String** | Cannot start with underscore. Maximum length &#x3D; 80 chars | 
**readOnly** | **Boolean** |  |  [optional]
**regex** | [**Pattern**](Pattern.md) |  |  [optional]
**searchable** | **Boolean** |  |  [optional]
**type** | [**TypeEnum**](#TypeEnum) |  |  [optional]
**unique** | **Boolean** |  |  [optional]


<a name="TypeEnum"></a>
## Enum: TypeEnum
Name | Value
---- | -----
TEXT | &quot;TEXT&quot;
NUMBER | &quot;NUMBER&quot;
LONG_NUMBER | &quot;LONG_NUMBER&quot;
JSON | &quot;JSON&quot;
DATE | &quot;DATE&quot;
BOOL | &quot;BOOL&quot;



