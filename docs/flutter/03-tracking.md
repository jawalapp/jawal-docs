# Tracking

!!! warning
    Calling the SDK's startTracking method without requesting the necessary permissions will cause the SDK to throw an exception.
    We recommend this package to handle the permissions for you: [https://pub.dev/packages/permission_handler](https://pub.dev/packages/permission_handler)

## Start tracking

Simply call the `Jawal.startTracking()` method to start tracking the user's location.

```dart
Jawal.startTracking()
//or
Jawal.startTracking("SESSION_ID")
```

!!! note
    The `SESSION_ID` parameter is optional and it's used to query the session's API to easily get the session's data.
    if your app has some kind of trip management system, you can use the trip's ID as the `SESSION_ID` to easily get the trip's data.

## Stop tracking

Simply call the `Jawal.stopTracking()` method to stop tracking the user's location.

```swift
Jawal.stopTracking()
```

## Check if the SDK is tracking

You can check if the SDK is tracking the user's location by calling the `Jawal.isTracking()` method.

```swift
let isTracking = Jawal.isTracking()
```
