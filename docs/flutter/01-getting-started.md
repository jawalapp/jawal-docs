# Getting Started

## Installation

The Jawal flutter SDK is available through [pub.dev](https://pub.dev/). To install it, simply add the following line to your `pubspec.yaml` file:

```yaml
dependencies:
  jawal_flutter: ^1.0.4
```

Once you have added the dependency, you can import the SDK into your project:

```dart
import 'package:jawal_flutter/jawal.dart';
```

## Initialization

We recommend that you initialize the SDK in the `main()` method of your `main.dart` file:

```dart
JawalConfig config = JawalConfig(
    apiKey: "YOUR_API_KEY",
    userId: "USER_UNIQUE_ID", 
    userDescription: "USER_DESCRIPTION", // Optional
    distanceFilter: 50, // Optional
    enableBackgroundTracking: true, // Optional
    interval: 1000, // Optional (android only)
    onInitResult: (InitResultEvent event) {
        if(event.isSuceessful) {
            /// SDK is initialized successfully
        } else {
            /// You can get the error message from event.error
            print(event.error);
        }
    },
);
Jawal.init(config);
```

`USER_UNIQUE_ID`: A unique ID for the user, it can be the user ID in your database
`USER_DESCRIPTION`: A description for the user, it can be the user name

See the [Configuration](/flutter/02-configuration/) page for a list of all available configuration options.
