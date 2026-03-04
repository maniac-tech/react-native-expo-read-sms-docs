---
sidebar_position: 2
---

# Upgrade to v9.1.x

## Overview

v9.1.x adds support for Expo SDK 51–54 and fixes compatibility issues with newer versions of React Native.

## What's Changed

- `minSdkVersion` raised from `21` to `23` (Android 6.0) — required by React Native 0.74+
- `compileSdk` and `targetSdkVersion` are now dynamic, deferring to your app's values
- `react-native` peer dependency changed from `*` to `>=0.73`
- Removed deprecated `createJSModules()` method

## Steps

### 1. Update the library

```bash
npm install @maniac-tech/react-native-expo-read-sms@latest
```

### 2. Update `app.json`

If you are using `expo-build-properties`, ensure your `minSdkVersion` is at least `23`:

```json
[
  "expo-build-properties",
  {
    "android": {
      "minSdkVersion": 23
    }
  }
]
```

### 3. Rebuild

```bash
npx expo prebuild --clean --platform android
npm run android
```

## Supported SDK Versions

| Expo SDK | React Native |
|----------|-------------|
| 44 – 50  | Legacy (v9.0.x) |
| 51       | 0.74 |
| 52       | 0.76 |
| 53       | 0.79 |
| 54       | 0.81 |
