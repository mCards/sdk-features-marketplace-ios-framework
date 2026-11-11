# mCards Features Marketplace SDK for iOS

Customer distribution of **FMSDK 1.3.13**, tested with **CoreSDK 1.4.8**.
Requires iOS 14 or later.

The SDK provides feature discovery and management, secure WebView features, and native
features such as send funds, card controls, points conversion, locations/offers and gifts.
Feature availability depends on the card program.

## Install with Swift Package Manager

1. Add `https://github.com/mCards/sdk-features-marketplace-ios-framework` at version
   **1.3.13** and select the `FMSDK` product.
2. Add `https://github.com/mCards/sdk-cards-ios-framework` at version **1.1.19** and
   select its `CoreSDK` product for the shared models. If the app already uses that
   package's `CardsSDK` product, CoreSDK is already supplied.
3. Remove any separate older CoreSDK/model package reference to avoid duplicate modules.

No Wantsa repository access is required. Applications that do not use card features can
select just the `CoreSDK` product from the Cards package.

```swift
import FMSDK
import CoreSDK
```

Configure `FmSdkProvider.shared` with valid cardholder `JWTs` and an
`FMSDKTokenRefreshCallback` before calling feature methods. Implement the callback to
return refreshed access and ID tokens; AuthSDK can be used as the token provider.
Use the credentials and environment assigned to your program.

[SDK documentation](https://mcards.readme.io/docs/mcards-sdk-overview)

## Release provenance

The XCFramework is copied unchanged from the pinned reference release recorded in
`RELEASE.json`; `.source-revision` records its source commit. Only customer-facing packaging
and documentation are maintained here. After merging the update, tag the merge commit
`1.3.13` to make this version available through Swift Package Manager.
