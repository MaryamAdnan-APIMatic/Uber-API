# Getting Started with Uber API

## Getting Started

### Introduction

Move your app forward with the Uber API

### Building

The generated code uses a few Maven dependencies e.g., Jackson, OkHttp,
and Apache HttpClient. The reference to these dependencies is already
added in the pom.xml file will be installed automatically. Therefore,
you will need internet access for a successful build.

* In order to open the client library in Eclipse click on `File -> Import`.

![Importing SDK into Eclipse - Step 1](https://apidocs.io/illustration/java?workspaceFolder=Uber%20API-Java&workspaceName=UberAPI&projectName=UberAPILib&rootNamespace=com.uber.api&groupId=UberAPILib&artifactId=uber-apilib&version=1.0.0&step=import0)

* In the import dialog, select `Existing Java Project` and click `Next`.

![Importing SDK into Eclipse - Step 2](https://apidocs.io/illustration/java?workspaceFolder=Uber%20API-Java&workspaceName=UberAPI&projectName=UberAPILib&rootNamespace=com.uber.api&groupId=UberAPILib&artifactId=uber-apilib&version=1.0.0&step=import1)

* Browse to locate the folder containing the source code. Select the detected location of the project and click `Finish`.

![Importing SDK into Eclipse - Step 3](https://apidocs.io/illustration/java?workspaceFolder=Uber%20API-Java&workspaceName=UberAPI&projectName=UberAPILib&rootNamespace=com.uber.api&groupId=UberAPILib&artifactId=uber-apilib&version=1.0.0&step=import2)

* Upon successful import, the project will be automatically built by Eclipse after automatically resolving the dependencies.

![Importing SDK into Eclipse - Step 4](https://apidocs.io/illustration/java?workspaceFolder=Uber%20API-Java&workspaceName=UberAPI&projectName=UberAPILib&rootNamespace=com.uber.api&groupId=UberAPILib&artifactId=uber-apilib&version=1.0.0&step=import3)

### Installation

The following section explains how to use the UberAPILib library in a new project.

#### 1. Starting a new project

For starting a new project, click the menu command `File > New > Project`.

![Add a new project in Eclipse](https://apidocs.io/illustration/java?workspaceFolder=Uber%20API-Java&workspaceName=UberAPI&projectName=UberAPILib&rootNamespace=com.uber.api&groupId=UberAPILib&artifactId=uber-apilib&version=1.0.0&step=createNewProject0)

Next, choose `Maven > Maven Project` and click `Next`.

![Create a new Maven Project - Step 1](https://apidocs.io/illustration/java?workspaceFolder=Uber%20API-Java&workspaceName=UberAPI&projectName=UberAPILib&rootNamespace=com.uber.api&groupId=UberAPILib&artifactId=uber-apilib&version=1.0.0&step=createNewProject1)

Here, make sure to use the current workspace by choosing `Use default Workspace location`, as shown in the picture below and click `Next`.

![Create a new Maven Project - Step 2](https://apidocs.io/illustration/java?workspaceFolder=Uber%20API-Java&workspaceName=UberAPI&projectName=UberAPILib&rootNamespace=com.uber.api&groupId=UberAPILib&artifactId=uber-apilib&version=1.0.0&step=createNewProject2)

Following this, select the *quick start* project type to create a simple project with an existing class and a `main` method. To do this, choose `maven-archetype-quickstart` item from the list and click `Next`.

![Create a new Maven Project - Step 3](https://apidocs.io/illustration/java?workspaceFolder=Uber%20API-Java&workspaceName=UberAPI&projectName=UberAPILib&rootNamespace=com.uber.api&groupId=UberAPILib&artifactId=uber-apilib&version=1.0.0&step=createNewProject3)

In the last step, provide a `Group Id` and `Artifact Id` as shown in the picture below and click `Finish`.

![Create a new Maven Project - Step 4](https://apidocs.io/illustration/java?workspaceFolder=Uber%20API-Java&workspaceName=UberAPI&projectName=UberAPILib&rootNamespace=com.uber.api&groupId=UberAPILib&artifactId=uber-apilib&version=1.0.0&step=createNewProject4)

#### 2. Add reference of the library project

The created Maven project manages its dependencies using its `pom.xml` file. In order to add a dependency on the *UberAPILib* client library, double click on the `pom.xml` file in the `Package Explorer`. Opening the `pom.xml` file will render a graphical view on the canvas. Here, switch to the `Dependencies` tab and click the `Add` button as shown in the picture below.

![Adding dependency to the client library - Step 1](https://apidocs.io/illustration/java?workspaceFolder=Uber%20API-Java&workspaceName=UberAPI&projectName=UberAPILib&rootNamespace=com.uber.api&groupId=UberAPILib&artifactId=uber-apilib&version=1.0.0&step=testProject0)

Clicking the `Add` button will open a dialog where you need to specify UberAPILib in `Group Id`, uber-apilib in `Artifact Id` and 1.0.0 in the `Version` fields. Once added click `OK`. Save the `pom.xml` file.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/java?workspaceFolder=Uber%20API-Java&workspaceName=UberAPI&projectName=UberAPILib&rootNamespace=com.uber.api&groupId=UberAPILib&artifactId=uber-apilib&version=1.0.0&step=testProject1)

![Adding sample code](https://apidocs.io/illustration/java?workspaceFolder=Uber%20API-Java&workspaceName=UberAPI&projectName=UberAPILib&rootNamespace=com.uber.api&groupId=UberAPILib&artifactId=uber-apilib&version=1.0.0&step=testProject2)

#### 3. Write sample code

Once the `SimpleConsoleApp` is created, a file named `App.java` will be visible in the *Package Explorer* with a `main` method. This is the entry point for the execution of the created project.
Here, you can add code to initialize the client library and instantiate a *Controller* class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

### Initialize the API Client

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| `timeout` | `long` | The timeout to use for making HTTP requests.<br>*Default*: `0L` |
| `httpClientConfig` | `ReadonlyHttpClientConfiguration` | Http Client Configuration instance. |

The API client can be initialized as follows:

```java
UberAPIClient client = new UberAPIClient.Builder()
    .build();
```

### Test the SDK

The generated code and the server can be tested using automatically generated test cases.
JUnit is used as the testing framework and test runner.

In Eclipse, for running the tests do the following:

1. Select the project UberAPILib from the package explorer.
2. Select `Run -> Run as -> JUnit Test` or use `Alt + Shift + X` followed by `T` to run the Tests.

## Client Class Documentation

### Uber APIClient Class

The gateway for the SDK. This class acts as a factory for the Controllers and also holds the configuration of the SDK.

#### Controllers

| Name | Description | Return Type |
|  --- | --- | --- |
| `getProductsController()` | Provides access to Products controller. | `ProductsController` |
| `getEstimatesController()` | Provides access to Estimates controller. | `EstimatesController` |
| `getUserController()` | Provides access to User controller. | `UserController` |

#### Methods

| Name | Description | Return Type |
|  --- | --- | --- |
| `shutdown()` | Shutdown the underlying HttpClient instance. | `void` |
| `getEnvironment()` | Current API environment. | `Environment` |
| `getHttpClient()` | The HTTP Client instance to use for making HTTP requests. | `HttpClient` |
| `getTimeout()` | The timeout to use for making HTTP requests. | `long` |
| `getHttpClientConfig()` | Http Client Configuration instance. | `ReadonlyHttpClientConfiguration` |
| `getBaseUri(Server server)` | Get base URI by current environment | `String` |
| `getBaseUri()` | Get base URI by current environment | `String` |

## API Reference

### List of APIs

* [Products](#products)
* [Estimates](#estimates)
* [User](#user)

### Products

#### Overview

##### Get instance

An instance of the `ProductsController` class can be accessed from the API Client.

```
ProductsController productsController = client.getProductsController();
```

#### Product Types

The Products endpoint returns information about the Uber products offered at a given location. The response includes the display name and other details about each product, and lists the products in the proper display order.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ProductList> productTypesAsync(
    final double latitude,
    final double longitude)
```

##### Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `latitude` | `double` | Query, Required | Latitude component of location. |
| `longitude` | `double` | Query, Required | Longitude component of location. |

##### Response Type

[`ProductList`](#product-list)

##### Example Usage

```java
double latitude = 65.76;
double longitude = 188.04;

productsController.productTypesAsync(latitude, longitude).thenAccept(result -> {
    // TODO success callback handler
}).exceptionally(exception -> {
    // TODO failure callback handler
    return null;
});
```

##### Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Unexpected error | [`ErrorException`](#error) |

### Estimates

#### Overview

##### Get instance

An instance of the `EstimatesController` class can be accessed from the API Client.

```
EstimatesController estimatesController = client.getEstimatesController();
```

#### Price Estimates

The Price Estimates endpoint returns an estimated price range for each product offered at a given location. The price estimate is provided as a formatted string with the full price range and the localized currency symbol.<br><br>The response also includes low and high estimates, and the [ISO 4217](http://en.wikipedia.org/wiki/ISO_4217) currency code for situations requiring currency conversion. When surge is active for a particular product, its surge_multiplier will be greater than 1, but the price estimate already factors in this multiplier.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<List<PriceEstimate>> priceEstimatesAsync(
    final double startLatitude,
    final double startLongitude,
    final double endLatitude,
    final double endLongitude)
```

##### Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `startLatitude` | `double` | Query, Required | Latitude component of start location. |
| `startLongitude` | `double` | Query, Required | Longitude component of start location. |
| `endLatitude` | `double` | Query, Required | Latitude component of end location. |
| `endLongitude` | `double` | Query, Required | Longitude component of end location. |

##### Response Type

[`List<PriceEstimate>`](#price-estimate)

##### Example Usage

```java
double startLatitude = 163.52;
double startLongitude = 96.76;
double endLatitude = 243.82;
double endLongitude = 205.12;

estimatesController.priceEstimatesAsync(startLatitude, startLongitude, endLatitude, endLongitude).thenAccept(result -> {
    // TODO success callback handler
}).exceptionally(exception -> {
    // TODO failure callback handler
    return null;
});
```

##### Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Unexpected error | [`ErrorException`](#error) |

#### Time Estimates

The Time Estimates endpoint returns ETAs for all products offered at a given location, with the responses expressed as integers in seconds. We recommend that this endpoint be called every minute to provide the most accurate, up-to-date ETAs.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<List<Product>> timeEstimatesAsync(
    final double startLatitude,
    final double startLongitude,
    final UUID customerUuid,
    final String productId)
```

##### Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `startLatitude` | `double` | Query, Required | Latitude component of start location. |
| `startLongitude` | `double` | Query, Required | Longitude component of start location. |
| `customerUuid` | `UUID` | Query, Optional | Unique customer identifier to be used for experience customization. |
| `productId` | `String` | Query, Optional | Unique identifier representing a specific product for a given latitude & longitude. |

##### Response Type

[`List<Product>`](#product)

##### Example Usage

```java
double startLatitude = 163.52;
double startLongitude = 96.76;

estimatesController.timeEstimatesAsync(startLatitude, startLongitude, null, null).thenAccept(result -> {
    // TODO success callback handler
}).exceptionally(exception -> {
    // TODO failure callback handler
    return null;
});
```

##### Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Unexpected error | [`ErrorException`](#error) |

### User

#### Overview

##### Get instance

An instance of the `UserController` class can be accessed from the API Client.

```
UserController userController = client.getUserController();
```

#### User Profile

The User Profile endpoint returns information about the Uber user that has authorized with the application.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<Profile> userProfileAsync()
```

##### Response Type

[`Profile`](#profile)

##### Example Usage

```java
userController.userProfileAsync().thenAccept(result -> {
    // TODO success callback handler
}).exceptionally(exception -> {
    // TODO failure callback handler
    return null;
});
```

##### Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Unexpected error | [`ErrorException`](#error) |

#### User Activity

The User Activity endpoint returns data about a user's lifetime activity with Uber. The response will include pickup locations and times, dropoff locations and times, the distance of past requests, and information about which products were requested.<br><br>The history array in the response will have a maximum length based on the limit parameter. The response value count may exceed limit, therefore subsequent API requests may be necessary.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<Activities> userActivityAsync(
    final Integer offset,
    final Integer limit)
```

##### Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `offset` | `Integer` | Query, Optional | Offset the list of returned results by this amount. Default is zero. |
| `limit` | `Integer` | Query, Optional | Number of items to retrieve. Default is 5, maximum is 100. |

##### Response Type

[`Activities`](#activities)

##### Example Usage

```java
userController.userActivityAsync(null, null).thenAccept(result -> {
    // TODO success callback handler
}).exceptionally(exception -> {
    // TODO failure callback handler
    return null;
});
```

##### Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Unexpected error | [`ErrorException`](#error) |

## Model Reference

### Structures

* [Product](#product)
* [Product List](#product-list)
* [Price Estimate](#price-estimate)
* [Profile](#profile)
* [Activity](#activity)
* [Activities](#activities)

#### Product

##### Class Name

`Product`

##### Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ProductId` | `String` | Optional | Unique identifier representing a specific product for a given latitude & longitude. For example, uberX in San Francisco will have a different product_id than uberX in Los Angeles. | String getProductId() | setProductId(String productId) |
| `Description` | `String` | Optional | Description of product. | String getDescription() | setDescription(String description) |
| `DisplayName` | `String` | Optional | Display name of product. | String getDisplayName() | setDisplayName(String displayName) |
| `Capacity` | `Integer` | Optional | Capacity of product. For example, 4 people. | Integer getCapacity() | setCapacity(Integer capacity) |
| `Image` | `String` | Optional | Image URL representing the product. | String getImage() | setImage(String image) |

##### Example (as JSON)

```json
{
  "product_id": null,
  "description": null,
  "display_name": null,
  "capacity": null,
  "image": null
}
```

#### Product List

##### Class Name

`ProductList`

##### Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Products` | [`List<Product>`](#product) | Optional | Contains the list of products | List<Product> getProducts() | setProducts(List<Product> products) |

##### Example (as JSON)

```json
{
  "products": null
}
```

#### Price Estimate

##### Class Name

`PriceEstimate`

##### Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ProductId` | `String` | Optional | Unique identifier representing a specific product for a given latitude & longitude. For example, uberX in San Francisco will have a different product_id than uberX in Los Angeles | String getProductId() | setProductId(String productId) |
| `CurrencyCode` | `String` | Optional | [ISO 4217](http://en.wikipedia.org/wiki/ISO_4217) currency code. | String getCurrencyCode() | setCurrencyCode(String currencyCode) |
| `DisplayName` | `String` | Optional | Display name of product. | String getDisplayName() | setDisplayName(String displayName) |
| `Estimate` | `String` | Optional | Formatted string of estimate in local currency of the start location. Estimate could be a range, a single number (flat rate) or "Metered" for TAXI. | String getEstimate() | setEstimate(String estimate) |
| `LowEstimate` | `Double` | Optional | Lower bound of the estimated price. | Double getLowEstimate() | setLowEstimate(Double lowEstimate) |
| `HighEstimate` | `Double` | Optional | Upper bound of the estimated price. | Double getHighEstimate() | setHighEstimate(Double highEstimate) |
| `SurgeMultiplier` | `Double` | Optional | Expected surge multiplier. Surge is active if surge_multiplier is greater than 1. Price estimate already factors in the surge multiplier. | Double getSurgeMultiplier() | setSurgeMultiplier(Double surgeMultiplier) |

##### Example (as JSON)

```json
{
  "product_id": null,
  "currency_code": null,
  "display_name": null,
  "estimate": null,
  "low_estimate": null,
  "high_estimate": null,
  "surge_multiplier": null
}
```

#### Profile

##### Class Name

`Profile`

##### Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `FirstName` | `String` | Optional | First name of the Uber user. | String getFirstName() | setFirstName(String firstName) |
| `LastName` | `String` | Optional | Last name of the Uber user. | String getLastName() | setLastName(String lastName) |
| `Email` | `String` | Optional | Email address of the Uber user | String getEmail() | setEmail(String email) |
| `Picture` | `String` | Optional | Image URL of the Uber user. | String getPicture() | setPicture(String picture) |
| `PromoCode` | `String` | Optional | Promo code of the Uber user. | String getPromoCode() | setPromoCode(String promoCode) |

##### Example (as JSON)

```json
{
  "first_name": null,
  "last_name": null,
  "email": null,
  "picture": null,
  "promo_code": null
}
```

#### Activity

##### Class Name

`Activity`

##### Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Uuid` | `String` | Optional | Unique identifier for the activity | String getUuid() | setUuid(String uuid) |

##### Example (as JSON)

```json
{
  "uuid": null
}
```

#### Activities

##### Class Name

`Activities`

##### Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Offset` | `Integer` | Optional | Position in pagination. | Integer getOffset() | setOffset(Integer offset) |
| `Limit` | `Integer` | Optional | Number of items to retrieve (100 max). | Integer getLimit() | setLimit(Integer limit) |
| `Count` | `Integer` | Optional | Total number of items available. | Integer getCount() | setCount(Integer count) |
| `History` | [`List<Activity>`](#activity) | Optional | - | List<Activity> getHistory() | setHistory(List<Activity> history) |

##### Example (as JSON)

```json
{
  "offset": null,
  "limit": null,
  "count": null,
  "history": null
}
```

### Exceptions

* [Error](#error)

#### Error

##### Class Name

`ErrorException`

##### Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Code` | `String` | Optional | - | String getCode() | setCode(String code) |
| `Message` | `String` | Optional | - | String getMessage() | setMessage(String message) |
| `Fields` | `String` | Optional | - | String getFields() | setFields(String fields) |

##### Example (as JSON)

```json
{
  "code": null,
  "message": null,
  "fields": null
}
```

## Utility Classes Documentation

### ApiHelper Class

This is a Helper class with commonly used utilities for the SDK.

#### Fields

| Name | Description | Type |
|  --- | --- | --- |
| mapper | Deserialization of Json data. | `ObjectMapper` |

#### Methods

| Name | Description | Return Type |
|  --- | --- | --- |
| `serialize(Object obj)` | Json Serialization of a given object. | `String` |
| `deserialize(String json)` | Json deserialization of the given Json string. | `LinkedHashMap<String, Object>` |
| `deserialize(String json, Class<T> clazz)` | Json deserialization of the given Json string. | `<T extends Object> T` |
| `deserialize(String json, TypeReference<T> typeReference)` | JSON Deserialization of the given json string. | `<T extends Object> T` |
| `deserializeArray(String json, Class<T[]> classArray)` | JSON Deserialization of the given json string. | `<T extends Object> List<T>` |

### FileWrapper Class

Class to wrap file and contentType to be sent as part of a HTTP request.

#### Constructors

| Name | Description |
|  --- | --- |
| `FileWrapper(File file)` | Initialization constructor. |
| `FileWrapper(File file, String contentType)` | Initialization constructor. |

#### Methods

| Name | Description | Return Type |
|  --- | --- | --- |
| `getFile()` | File instance. | `File` |
| `getContentType()` | Content type of the file. | `String` |

## Common Code Documentation

### HttpRequest Class

Class for creating and managing HTTP Requests.

#### Constructors

| Name | Description |
|  --- | --- |
| `HttpRequest(HttpMethod method, StringBuilder queryUrlBuilder, Headers headers, Map<String, Object> queryParameters, List< SimpleEntry < String, Object >> parameters)` | Initializes a simple http request. |

#### Methods

| Name | Description | Return Type |
|  --- | --- | --- |
| `getHttpMethod()` | HttpMethod for the http request. | `HttpMethod` |
| `getHeaders()` | Headers for the http request. | `Headers` |
| `getQueryUrl()` | Query url for the http request. | `String` |
| `getParameters()` | Parameters for the http request. | `List<SimpleEntry<String, Object>>` |
| `getQueryParameters()` | Query parameters for the http request. | `Map<String, Object>` |
| `addQueryParameter(String key, Object value)` | Add Query parameter in http request. | `void` |

### HttpResponse Class

Class to hold HTTP Response.

#### Constructors

| Name | Description |
|  --- | --- |
| `HttpResponse(int code, Headers headers, InputStream rawBody)` | Constructor for HttpResponse. |

#### Methods

| Name | Description | Return Type |
|  --- | --- | --- |
| `getStatusCode()` | HTTP Status code of the http response.. | `int` |
| `getHeaders()` | Headers of the http response. | `Headers` |
| `getRawBody()` | Raw body of the http response. | `InputStream` |

### HttpStringResponse Class

Class to hold response body as string.

#### Constructors

| Name | Description |
|  --- | --- |
| `HttpStringResponse(int code, Headers headers, InputStream rawBody, String body)` | Constructor for HttpStringResponse. |

#### Methods

| Name | Description | Return Type |
|  --- | --- | --- |
| `getStatusCode()` | HTTP Status code of the http response. | `int` |
| `getHeaders()` | Headers of the http response. | `Headers` |
| `getBody()` | String body of the http response. | `String` |

### HttpContext Class

Class to wrap the request sent to the server and the response received from the server.

#### Constructors

| Name | Description |
|  --- | --- |
| `HttpContext(HttpRequest request, HttpResponse response)` | Constructor for HttpContext. |

#### Methods

| Name | Description | Return Type |
|  --- | --- | --- |
| `getRequest()` | Getter for the Http Request. | `HttpRequest` |
| `getHttpContext()` | Getter for the Http Response. | `HttpContext` |

### HttpBodyRequest Class

HTTP Request with an explicit body.

#### Constructors

| Name | Description |
|  --- | --- |
| `HttpBodyRequest(HttpMethod method, StringBuilder queryUrlBuilder, Headers headers, Map<String, Object> queryParams, Object body)` | Create a request with explicit body. |

#### Methods

| Name | Description | Return Type |
|  --- | --- | --- |
| `getBody()` | Body for the http request. | `Object` |

### HttpCallback Interface

Callback to be called before and after the HTTP call for an endpoint is made.

#### Methods

| Name | Description | Return Type |
|  --- | --- | --- |
| `onBeforeRequest(HttpRequest request)` | Callback called just before the HTTP request is sent. | `void` |
| `onAfterResponse(HttpContext context)` | Callback called just after the HTTP response is received. | `void` |

### Headers Class

Class for creating and managing HTTP Headers.

#### Constructors

| Name | Description |
|  --- | --- |
| `Headers()` | Default constructor. |
| `Headers(Map<String, List<String>> headers)` | Constructor that creates a new instance using a given Map. |
| `Headers(Headers h)` | Copy Constructor. |

#### Methods

| Name | Description | Return Type |
|  --- | --- | --- |
| `has(String headerName)` | Use to check if the given name is present in headers. | `boolean` |
| `names()` | Returns a Set containing all header names. | `Set<String>` |
| `value(String headerName)` | Returns the first value associated with a given header name, or null if the header name is not found. | `String` |
| `values(String headerName)` | Returns a List of all values associated with a given header name, or null if the header name is not found. | `List<String>` |
| `asSimpleMap()` | Returns a Map of the headers, giving only one value for each header name. | `Map<String, String>` |
| `asMultimap()` | Returns a simulated MultiMap of the headers. | `Map<String, List<String>>` |
| `cloneHeaderMap(Map<String, List<String>> headerMap)` | Clones a header map. | `Map<String, List<String>>` |
| `add(String headerName, String value)` | Adds a value for a header name to this object. | `void` |
| `add(String headerName, List<String> values)` | Adds a List of values for a header name to this object. | `void` |
| `addAllFromMap(Map<String, String> headers)` | Adds values from a Map to this object. | `void` |
| `addAllFromMultiMap(Map<String, List<String>> headers)` | Adds values from a simulated Multi-Map to this object. | `void` |
| `addAll(Headers headers)` | Adds all the entries in a Headers object to this object. | `void` |
| `remove(String headerName)` | Removes the mapping for a header name if it is present. | `List<String>` |

### ApiException Class

This is the base class for all exceptions that represent an error response from the server.

#### Constructors

| Name | Description |
|  --- | --- |
| `ApiException(String reason)` | Initialization constructor. |
| `ApiException(String reason, HttpContext context)` | Initialization constructor. |

#### Methods

| Name | Description | Return Type |
|  --- | --- | --- |
| `getResponseCode()` | The HTTP response code from the API request | `int` |
| `getHeaders()` | The HTTP response body from the API request. | `Headers` |

### Configuration Interface

This is the base class for all exceptions that represent an error response from the server.

#### Methods

| Name | Description | Return Type |
|  --- | --- | --- |
| `getEnvironment()` | Current API environment. | `Environment` |
| `getTimeout()` | The timeout to use for making HTTP requests. | `long` |
| `getHttpClientConfig()` | Http Client Configuration instance. | `ReadonlyHttpClientConfiguration` |
| `getBaseUri(Server server)` | Get base URI by current environment. | `String` |
| `getBaseUri()` | Get base URI by current environment. | `String` |

