# LoggingOSLog

[OSLog](https://developer.apple.com/documentation/os/oslog) logging backend for [swift-log](https://github.com/apple/swift-log).

## Getting Started

Add as a dependency in your `Package.swift`:

```swift
.package(url: "https://github.com/chrisaljoudi/swift-log-oslog.git", .from("0.1.0"))
```

## Usage

During app startup/initialization:

```swift
import Logging
import LoggingSyslog

/// Configure logging system to use OSLog logging backend
LoggingSystem.bootstrap(LoggingOSLog.init)
```

Then:
```swift
let logger = Logger(label: "com.yourcompany.yourawesomeapp")

/// ...

logger.info("Unified Logging is pretty cool.")
```

