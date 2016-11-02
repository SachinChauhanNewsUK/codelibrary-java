# Zuora REST API Code Library in Java

The code libraries, including any sample code, are provided “AS IS”, for demonstration purposes only. Zuora does not guarantee or make any representations regarding the use, results of use, accuracy, security, timeliness, or completeness of any data or information relating to the sample code. You, the customer, are responsible for making sure that your implementation is functional and secure.

Go to [Zuora Community](http://community.zuora.com/) to report issues or discuss these samples with your peers.

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

import io.swagger.client.*;
import io.swagger.client.auth.*;
import io.swagger.client.model.*;
import io.swagger.client.api.AccountingCodesApi;

import java.io.File;
import java.util.*;

public class AccountingCodesApiExample {

    public static void main(String[] args) {
        
        AccountingCodesApi apiInstance = new AccountingCodesApi();
        String acId = "acId_example"; // String | ID of the accounting code you want to delete.
        try {
            CommonResponseType result = apiInstance.dELETEAccountingCode(acId);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling AccountingCodesApi#dELETEAccountingCode");
            e.printStackTrace();
        }
    }
}

```

## Documentation for API Endpoints

All documentation can be found in the Developer Center, in the [API Reference](https://www.zuora.com/developer/api-reference/).

## Recommendation

It's recommended to create an instance of `ApiClient` per thread in a multithreaded environment to avoid any potential issues.

## Author

docs@zuora.com

