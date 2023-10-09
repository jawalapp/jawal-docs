# Tracking

After initializing the SDK and requesting the required permissions, you can start tracking the user's location.

!!! warning
    Make sure that the app has the [necessary permissions](https://developer.android.com/training/location/permissions) to track the user's location.

## Start tracking

Simply call the `Jawal.startTracking()` method to start tracking the user's location.

```java
Jawal.startTracking()
//or 
Jawal.startTracking("SESSION_ID")
```

!!! note
    The `SESSION_ID` parameter is optional and it's used to query the session's API to easily get the session's data.
    if your app has some kind of trip management system, you can use the trip's ID as the `SESSION_ID` to easily get the trip's data.

## Stop tracking

Simply call the `Jawal.stopTracking()` method to stop tracking the user's location.

```java
Jawal.stopTracking()
```

!!! info
    The SDK will automatically start tracking after initialization, so you don't need to call `Jawal.startTracking()` after app restarts.
