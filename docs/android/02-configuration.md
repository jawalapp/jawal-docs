# Configuration

The `JawalConfig` object is used to configure the SDK. It can be created using the `JawalConfig.Builder` class.

```java
final config = JawalConfig.Builder()
    .setSdkKey("SDK_KEY")
    .setUserId("USER_ID")
    .build();
```

The `setSDKKey()` and `setUserId()` methods are required. The `USER_ID` must be a unique identifier for the user in the project (for example, a user ID from your database, email, username, etc...). The `SDK_KEY` is the project's SDK key, which can be found in the project's settings page in the dashboard.

## Optional configuration

The `JawalConfig` object also allows you to configure the following:

### `setDescription()`

```java
JawalConfig.Builder()
    ...
    .setDescription("John Doe")
    .build();
```

This method allows you to set a description for the user to identify them in the dashboard, for example, their name. The default value is `null`.

### `setTrackingDistance()`

```java
JawalConfig.Builder()
    ...
    .setTrackingDistance(10)
    .build();
```

This method allows you to set the minimum distance the user must travel before their location is tracked. The default value is `10` (10 meters).

### `enableBackgroundTracking()`

```java
JawalConfig.Builder()
    ...
    .enableBackgroundTracking(true)
    .build();
```

Enable the background tracking service. The default value is `false`.

!!! warning
    Enabling background tracking will cause the SDK to track the user's location even when the app is in the background. Make sure that you have the [necessary permissions](https://developer.android.com/training/location/background) to do this.
