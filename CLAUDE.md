# ReplySong

## Overview
Flutter mobile app under Ruvix Labs that turns message replies into AI-generated songs using the original words as lyrics.

Primary acquisition is expected to come from paid social, so the product should stay mobile-first, fast, emotionally obvious, and conversion-measured from first open through subscription and generation.

## Tech Stack
- **Framework**: Flutter
- **Platform**: iOS + Android
- **Business**: Ruvix Labs
- **Backend**: Firebase (project/app IDs to be created)
- **Subscriptions**: RevenueCat, mirroring the Ruvix Labs native subscription pattern
- **Music generation**: Kie.ai Suno API or the selected server-side generation provider
- **Analytics / Attribution**: Firebase Analytics for product events; Meta SDK/CAPI or mobile attribution tooling for paid-social conversion tracking

## Product Rules
1. Preserve the user's pasted messages as lyrics; do not paraphrase the source text.
2. Keep the mobile funnel fast: messages -> sound -> email/account -> paywall -> generation.
3. Do not start paid generation until RevenueCat confirms an active entitlement.
4. Treat ReplySong as the consumer mobile brand; do not expose internal provider names in the UI.

## Subscription Notes
- Use RevenueCat for native subscription entitlement management.
- Create separate iOS and Android app identifiers for ReplySong under Ruvix Labs.
- Do not reuse another app's bundle ID, package name, RevenueCat project ID, store product IDs, or credentials.
- RevenueCat setup depends on the native identifiers and store apps existing first.

## Project Structure
To be scaffolded with Flutter after this project shell.

Target shape:
```
ReplySong/
├── lib/
├── test/
├── ios/
├── android/
├── docs/
│   └── plans/
└── CLAUDE.md
```

## Commands
```bash
# After Flutter scaffold exists
flutter pub get
flutter analyze
flutter test
flutter run
```

## Environment Variables / Secrets
To be filled after Firebase, RevenueCat, and generation backend setup.

Never commit API keys, RevenueCat secret keys, App Store keys, Google Play credentials, or generated passwords.

## Notes
- Slack channel: `#replysong`
- GitHub: https://github.com/RuvixLabs/ReplySong
