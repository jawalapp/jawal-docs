# Configuration

the init method takes a config object that contains the following properties:


## sdk_key (required)

The SDK key of the project. You can find this in the project's settings page in the dashboard.

## user_id (required)

A unique identifier for the user in the project (for example, a user ID from your database, email, username, etc...).

## user_description (optional)

A description for the user to identify them in the dashboard, for example, their name.

## distanceFilter (optional)

The minimum distance the user must travel before their location is tracked. The default value is `50` (50 meters).

## enable_background_tracking (optional)

Enable the background tracking service. The default value is `false`.

!!! warning
    Enabling background tracking will cause the SDK to track the user's location even when the app is in the background. Make sure that you have the `Background modes` capability enabled in your app's `Signing & Capabilities` settings and the `Location updates` mode is checked.

    You can find more information about this [here](https://developer.apple.com/documentation/corelocation/getting_the_user_s_location/handling_location_events_in_the_background).
