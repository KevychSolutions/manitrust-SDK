# Manitrust
Github of Manitrust Service.

## Installation

##### CocoaPods 

[CocoaPods](https://cocoapods.org/) is a dependency manager for Cocoa projects. For usage and installation instructions, visit their website. To integrate GrowthBook into your Xcode project using CocoaPods, specify it in your `Podfile`:

- Add below in podfile - in respective target block

```swift
pod 'ManiTrust'
```

- Execute below command in terminal

```swift
pod install
```

##### Swift Package Manager - SPM

The [Swift Package Manager](https://swift.org/package-manager/) is a tool for automating the distribution of Swift code and is integrated into the `swift`compiler.

Once you have your Swift package set up, adding ManiTrust_SDK as a dependency is as easy as adding it to the `dependencies` value of your `Package.swift`.

```swift
dependencies: [
    .package(url: "https://github.com/KevychSolutions/manitrust-SDK.git")
]
```

## Setup project
reqistration in admin


## Integration 

1. create apns key
2. registrations in admin
3. add Notifications Service Extention
4. registered device in app `ManiTrustBuilder(projectID: "e4ecdf5c-33ad-4f70-9f42-58bf0edfb6da", apiKey: "ae1719f8a81c2ae9349888d0ed5c5d4d", token: deviceToken, phoneNumber: self.phoneNunber)`
5. add call function in method `didReceive` 
            `if let data = bestAttemptContent.userInfo["data"] as? [String: Any] {
                ManiTrustManager.shared.setupContact(contactData: data)
                contentHandler(bestAttemptContent)
            } else {
                ManiTrustManager.shared.setupContact(contactData: bestAttemptContent.userInfo)
                contentHandler(bestAttemptContent)
            } `

