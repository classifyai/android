# DefaultApi

All URIs are relative to *https://api.classifyai.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createNewModel**](DefaultApi.md#createNewModel) | **PUT** /models | Create New Model
[**deleteModel**](DefaultApi.md#deleteModel) | **DELETE** /models | Delete Model
[**getModelsList**](DefaultApi.md#getModelsList) | **GET** /models | Get Models List
[**indexByImageUrl**](DefaultApi.md#indexByImageUrl) | **POST** /index_by_image_url | Index by Using Image URL
[**indexImage**](DefaultApi.md#indexImage) | **POST** /index_image | Index Local Image
[**tagImageByUrl**](DefaultApi.md#tagImageByUrl) | **GET** /predict_by_image_url | Tag Image by Using Image Url
[**tagLocalImage**](DefaultApi.md#tagLocalImage) | **POST** /predict | Predict by Image
[**updateModel**](DefaultApi.md#updateModel) | **POST** /models | Update Model



## createNewModel

> createNewModel(modelName)

Create New Model

Create a new custom image recognition model

### Example

```java
// Import classes:
//import org.openapitools.client.api.DefaultApi;

DefaultApi apiInstance = new DefaultApi();
String modelName = {"model_name":"\"Test model name\""}; // String | Set a name for your model
try {
    apiInstance.createNewModel(modelName);
} catch (ApiException e) {
    System.err.println("Exception when calling DefaultApi#createNewModel");
    e.printStackTrace();
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **modelName** | **String**| Set a name for your model | [default to null]

### Return type

null (empty response body)

### Authorization

[x-api-key](../README.md#x-api-key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## deleteModel

> deleteModel(modelId)

Delete Model

Delete Model

### Example

```java
// Import classes:
//import org.openapitools.client.api.DefaultApi;

DefaultApi apiInstance = new DefaultApi();
String modelId = null; // String | You can find your model ids from Classify Dashboard.
try {
    apiInstance.deleteModel(modelId);
} catch (ApiException e) {
    System.err.println("Exception when calling DefaultApi#deleteModel");
    e.printStackTrace();
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **modelId** | **String**| You can find your model ids from Classify Dashboard. | [default to null]

### Return type

null (empty response body)

### Authorization

[x-api-key](../README.md#x-api-key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## getModelsList

> String getModelsList()

Get Models List

Get the list of of models created 

### Example

```java
// Import classes:
//import org.openapitools.client.api.DefaultApi;

DefaultApi apiInstance = new DefaultApi();
try {
    String result = apiInstance.getModelsList();
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DefaultApi#getModelsList");
    e.printStackTrace();
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

**String**

### Authorization

[x-api-key](../README.md#x-api-key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## indexByImageUrl

> indexByImageUrl(inlineObject)

Index by Using Image URL

Index by Using Image URL

### Example

```java
// Import classes:
//import org.openapitools.client.api.DefaultApi;

DefaultApi apiInstance = new DefaultApi();
InlineObject inlineObject = new InlineObject(); // InlineObject | 
try {
    apiInstance.indexByImageUrl(inlineObject);
} catch (ApiException e) {
    System.err.println("Exception when calling DefaultApi#indexByImageUrl");
    e.printStackTrace();
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inlineObject** | [**InlineObject**](InlineObject.md)|  |

### Return type

null (empty response body)

### Authorization

[x-api-key](../README.md#x-api-key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## indexImage

> String indexImage(modelId, tag, file)

Index Local Image

Index Local Image

### Example

```java
// Import classes:
//import org.openapitools.client.api.DefaultApi;

DefaultApi apiInstance = new DefaultApi();
String modelId = null; // String | 
String tag = null; // String | 
File file = null; // File | 
try {
    String result = apiInstance.indexImage(modelId, tag, file);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DefaultApi#indexImage");
    e.printStackTrace();
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **modelId** | **String**|  | [optional] [default to null]
 **tag** | **String**|  | [optional] [default to null]
 **file** | **File**|  | [optional] [default to null]

### Return type

**String**

### Authorization

[x-api-key](../README.md#x-api-key)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json


## tagImageByUrl

> tagImageByUrl(modelId, imageUrl)

Tag Image by Using Image Url

Predict image tags by providing image url

### Example

```java
// Import classes:
//import org.openapitools.client.api.DefaultApi;

DefaultApi apiInstance = new DefaultApi();
String modelId = null; // String | Type your trained model id to predict. You get your model's id from Classify Dashboard.
String imageUrl = null; // String | Provide image url to predict
try {
    apiInstance.tagImageByUrl(modelId, imageUrl);
} catch (ApiException e) {
    System.err.println("Exception when calling DefaultApi#tagImageByUrl");
    e.printStackTrace();
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **modelId** | **String**| Type your trained model id to predict. You get your model&#39;s id from Classify Dashboard. | [default to null]
 **imageUrl** | **String**| Provide image url to predict | [default to null]

### Return type

null (empty response body)

### Authorization

[x-api-key](../README.md#x-api-key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## tagLocalImage

> tagLocalImage(file, modelId)

Predict by Image

Send a local image to tag

### Example

```java
// Import classes:
//import org.openapitools.client.api.DefaultApi;

DefaultApi apiInstance = new DefaultApi();
File file = null; // File | 
String modelId = null; // String | 
try {
    apiInstance.tagLocalImage(file, modelId);
} catch (ApiException e) {
    System.err.println("Exception when calling DefaultApi#tagLocalImage");
    e.printStackTrace();
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file** | **File**|  | [optional] [default to null]
 **modelId** | **String**|  | [optional] [default to null]

### Return type

null (empty response body)

### Authorization

[x-api-key](../README.md#x-api-key)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json


## updateModel

> updateModel(modelName, modelId)

Update Model

Update Model Name

### Example

```java
// Import classes:
//import org.openapitools.client.api.DefaultApi;

DefaultApi apiInstance = new DefaultApi();
String modelName = null; // String | Model Name
String modelId = null; // String | Model id to be renamed.
try {
    apiInstance.updateModel(modelName, modelId);
} catch (ApiException e) {
    System.err.println("Exception when calling DefaultApi#updateModel");
    e.printStackTrace();
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **modelName** | **String**| Model Name | [default to null]
 **modelId** | **String**| Model id to be renamed. | [default to null]

### Return type

null (empty response body)

### Authorization

[x-api-key](../README.md#x-api-key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

