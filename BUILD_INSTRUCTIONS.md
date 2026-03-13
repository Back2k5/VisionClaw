# VisionClaw Build Instructions

## One-Step Build & Install (when iPhone is connected)

```bash
cd /Users/jetjohnson/.openclaw/workspace/projects/VisionClaw/samples/CameraAccess

# Build for Lee's iPhone
xcodebuild -scheme CameraAccess \
  -destination "id=00008150-000C74580284401C" \
  -configuration Debug \
  -allowProvisioningUpdates \
  DEVELOPMENT_TEAM=FXXHCX6FJ3 \
  build

# Install to device (after successful build)
xcrun devicectl device install app \
  --device 00008150-000C74580284401C \
  ~/Library/Developer/Xcode/DerivedData/CameraAccess-*/Build/Products/Debug-iphoneos/CameraAccess.app
```

## Device Info
- **Lee's iPhone**: `00008150-000C74580284401C` (iOS 26.0)
- **Team ID**: `FXXHCX6FJ3` (Jet Johnson Personal Team)
- **Bundle ID**: `com.jetplastics.VisionClaw`
- **Apple ID**: `jet@jetplastics.com`

## Prerequisites
- iPhone connected via USB with Developer Mode ON
- Xcode 26.3 with iOS platform installed ✅
- Apple ID signed into Xcode ✅
- Keychain access granted for code signing ✅

## If keychain prompt appears
Mac login password: stored in memory/sensitive/accounts.md (Machine Login section)
Click "Always Allow" to prevent future prompts.

## Gateway Config (already set)
- `gateway.bind: "lan"`
- `chatCompletions: enabled`
- Auth token set
- Secrets.swift configured with all credentials
