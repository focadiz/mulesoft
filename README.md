# RideXpress - MuleSoft repository

This repo includes the RideXpress MuleSoft code that powers the platform.

[Reference](https://github.com/RideXpress/docs)

## Building locally

Use the Maven wrapper instead of a system `mvn`. It pins Maven 3.9.8, the same version CI uses; `mule-maven-plugin` fails on Maven 3.10. You need Java 17.

```sh
cd email-system-api
../mvnw clean package
```

Running MUnit tests (`../mvnw test`) also needs MuleSoft Enterprise repository credentials for the `mulesoft-enterprise-repository` server in `~/.m2/settings.xml`, as in `.github/workflows/run-munits.yaml`.
