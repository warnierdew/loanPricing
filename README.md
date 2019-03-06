# spring-swagger-codegen-api-client

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
    <groupId>eu.eisti</groupId>
    <artifactId>spring-swagger-codegen-api-client</artifactId>
    <version>0.0.1-SNAPSHOT</version>
    <scope>compile</scope>
</dependency>
```

### Gradle users

Add this dependency to your project's build file:

```groovy
compile "eu.eisti:spring-swagger-codegen-api-client:0.0.1-SNAPSHOT"
```

### Others

At first generate the JAR by executing:

    mvn package

Then manually install the following JARs:

* target/spring-swagger-codegen-api-client-0.0.1-SNAPSHOT.jar
* target/lib/*.jar

## Getting Started

Please follow the [installation](#installation) instruction and execute the following Java code:

```java

import eu.eisti.calculation.client.invoker.*;
import eu.eisti.calculation.client.invoker.auth.*;
import eu.eisti.calculation.client.model.*;
import eu.eisti.calculation.client.api.PricingApi;

import java.io.File;
import java.util.*;

public class PricingApiExample {

    public static void main(String[] args) {
        
        PricingApi apiInstance = new PricingApi();
        PricingCriteria body = new PricingCriteria(); // PricingCriteria | ID of PricingId that needs to be updated
        try {
            Object result = apiInstance.updatePricingIdWithForm(body);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling PricingApi#updatePricingIdWithForm");
            e.printStackTrace();
        }
    }
}

```

## Documentation for API Endpoints

All URIs are relative to *https://petstore.swagger.io/v2*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*PricingApi* | [**updatePricingIdWithForm**](docs/PricingApi.md#updatePricingIdWithForm) | **POST** /pricing | Updates a Pricing form data


## Documentation for Models

 - [Pricing](docs/Pricing.md)
 - [PricingCriteria](docs/PricingCriteria.md)


## Documentation for Authorization

All endpoints do not require authorization.
Authentication schemes defined for the API:

## Recommendation

It's recommended to create an instance of `ApiClient` per thread in a multithreaded environment to avoid any potential issues.

## Author

apiteam@swagger.io

