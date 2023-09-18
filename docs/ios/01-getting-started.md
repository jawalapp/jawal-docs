# Getting Started


## Installation

The Jawal SDK is available through [CocoaPods](https://cocoapods.org/). To install it, simply add the following line to your Podfile:

```ruby
pod 'jawal-ios'
```

## Initialization

We recommend that you initialize the SDK in the `application(_:didFinishLaunchingWithOptions:)` method of your `AppDelegate`:

```swift
import JawalSwift

func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?) -> Bool {
    Jawal.start { config in
        config.sdk_key = "YOUR_SDK_KEY"
        config.user_id = "USER_ID"
    }
    return true
}
```

Optionally You can listen to the result of the initialization by passing a callback to the `start()` method:

```swift
Jawal.start { config in
    config.sdk_key = "YOUR_SDK_KEY"
    config.user_id = "USER_ID"
},
completion: { result in
    switch result {
    case .success:
        print("Jawal initialized successfully")
    case .failure(let error):
        print("Jawal failed to initialize: \(error)")
    }
}
```

See the [Configuration](/ios/02-configuration/) page for a list of all available configuration options.
