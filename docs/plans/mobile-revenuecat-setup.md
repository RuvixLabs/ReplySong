# ReplySong Mobile + RevenueCat Setup Plan

## Decisions
- Brand: ReplySong
- Business: Ruvix Labs
- Framework: Flutter
- Subscriptions: RevenueCat native subscriptions
- Billing policy: native IAP entitlement must be active before paid music generation starts

## Identifier Plan
- iOS bundle id: `com.ruvixlabs.replysong`
- Android package id: `com.ruvixlabs.replysong`
- RevenueCat project: `ReplySong`
- Entitlement suggestion: `pro`

These identifiers should be checked against App Store Connect, Google Play, Firebase, and RevenueCat before creation.

## Setup Order
1. Scaffold the Flutter app.
2. Create iOS bundle ID and Android package identity under Ruvix Labs.
3. Create Firebase project/apps for iOS and Android.
4. Create App Store Connect and Google Play app records.
5. Create RevenueCat project with iOS + Android apps.
6. Create subscription entitlement, offerings, packages, and store products.
7. Wire Flutter RevenueCat SDK and entitlement checks.
8. Gate generation API calls behind confirmed RevenueCat entitlement.
9. Add Firebase Analytics and paid-social attribution events.
10. Run sandbox purchase tests on iOS and Android.

## Open Questions
- Exact weekly/monthly/annual pricing shape.
- Whether to offer only weekly at launch or mirror a broader Ruvix Labs subscription pattern.
- Whether the generation backend reuses SongFromText Firebase/Kie services or gets a new Firebase/backend project.
