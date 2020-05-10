# openapi-android-client

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
    <groupId>org.openapitools</groupId>
    <artifactId>openapi-android-client</artifactId>
    <version>1.0.0</version>
    <scope>compile</scope>
</dependency>
```

### Gradle users

Add this dependency to your project's build file:

```groovy
compile "org.openapitools:openapi-android-client:1.0.0"
```

### Others

At first generate the JAR by executing:

    mvn package

Then manually install the following JARs:

- target/openapi-android-client-1.0.0.jar
- target/lib/*.jar

## Getting Started

Please follow the [installation](#installation) instruction and execute the following Java code:

```java

import org.openapitools.client.api.DefaultApi;

public class DefaultApiExample {

    public static void main(String[] args) {
        DefaultApi apiInstance = new DefaultApi();
        String modelName = {"model_name":"\"Test model name\""}; // String | Set a name for your model
        try {
            apiInstance.createNewModel(modelName);
        } catch (ApiException e) {
            System.err.println("Exception when calling DefaultApi#createNewModel");
            e.printStackTrace();
        }
    }
}

```

## Documentation for API Endpoints

All URIs are relative to *http://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*DefaultApi* | [**createNewModel**](docs/DefaultApi.md#createNewModel) | **PUT** /models | Create New Model
*DefaultApi* | [**deleteModel**](docs/DefaultApi.md#deleteModel) | **DELETE** /models | Delete Model
*DefaultApi* | [**getModelsList**](docs/DefaultApi.md#getModelsList) | **GET** /models | Get Models List
*DefaultApi* | [**tagImageByUrl**](docs/DefaultApi.md#tagImageByUrl) | **GET** /predict_by_image_url | Tag Image by Using Image Url
*DefaultApi* | [**tagLocalImage**](docs/DefaultApi.md#tagLocalImage) | **POST** /predict | Predict by Image
*DefaultApi* | [**updateModel**](docs/DefaultApi.md#updateModel) | **POST** /models | Update Model


## Documentation for Models

 - [InlineObject](docs/InlineObject.md)


## Documentation for Authorization

Authentication schemes defined for the API:
### x-api-key

- **Type**: API key

- **API key parameter name**: x-api-key
- **Location**: HTTP header


## Recommendation

It's recommended to create an instance of `ApiClient` per thread in a multithreaded environment to avoid any potential issues.

## Author

info@inoven.ai

