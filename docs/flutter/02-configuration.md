# Configuration

the init method takes a config object that contains the following properties:


## sdkKey (required)

The SDK key of the project. You can find this in the project's settings page in the dashboard.

## userId (required)

A unique identifier for the user in the project (for example, a user ID from your database, email, username, etc...).

## userDescription (optional)

A description for the user to identify them in the dashboard, for example, their name.

## distanceFilter (optional)

The minimum distance the user must travel before their location is tracked. The default value is `10` (10 meters).

## enableBackgroundTracking (optional)

Enable the background tracking service. The default value is `false`.

## interval (optional)

(android only) The interval between location updates in milliseconds. The default value is `1000` (1 second).

!!! warning
    Enabling background tracking will cause the SDK to track the user's location even when the app is in the background. Make sure that you have the neccessary permissions to do this (both iOS and Android).
