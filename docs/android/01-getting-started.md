# Getting Started

## Installation

The easiest way to install the SDK is to use the [Gradle](https://gradle.org/) dependency management system. To do this, add the following to your `build.gradle` file:

```groovy
repositories {
    ...
    maven {
        url "https://europe-west1-maven.pkg.dev/ace-ensign-383123/jawal-java"
    }
}
```

```groovy
dependencies {
    ...
    implementation 'com.yastack:jawal:0.0.1'
}
```

Once you have added the dependency, you can import the SDK into your project:

```java
import com.yastack:jawal.Jawal;
```

## Initialization

The SDK must be initialized before it can be used. This is done by calling the `Jawal.init()` method:

```java
Jawal.init(this, config);
```

See the [Configuration](configuration.md) page for more information about the `config` parameter.
