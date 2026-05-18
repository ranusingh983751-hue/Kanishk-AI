# GetRedeemCode - APK Build Guide
## Version 4.0 | Package: com.getredeemcode.app

---

## ✅ STEP 1: SDK Path Set Karo

`local.properties` file kholo aur apna Android SDK path likho:

**Windows:**
```
sdk.dir=C\:\\Users\\YourName\\AppData\\Local\\Android\\Sdk
```

**Mac/Linux:**
```
sdk.dir=/Users/YourName/Library/Android/sdk
```

---

## ✅ STEP 2: Android Studio Me Open Karo

1. Android Studio open karo
2. **File → Open** → Is folder ko select karo (`GetRedeemCode_APKReady`)
3. Gradle sync hone do (internet chahiye pehli baar)

---

## ✅ STEP 3: Debug APK Build Karo (Testing ke liye)

Menu se:
```
Build → Build Bundle(s) / APK(s) → Build APK(s)
```

APK milegi yahan:
```
app/build/outputs/apk/debug/app-debug.apk
```

---

## ✅ STEP 4: Release APK Build Karo (Play Store / Final)

Menu se:
```
Build → Generate Signed Bundle / APK → APK → Next
```

- Keystore create karo ya existing use karo
- Fill karo: Key alias, password
- Select **release** build variant
- Finish

Release APK milegi yahan:
```
app/build/outputs/apk/release/app-release.apk
```

---

## ✅ STEP 5: Command Line se Build (Optional)

```bash
# Debug APK
./gradlew assembleDebug

# Release APK (unsigned)
./gradlew assembleRelease
```

---

## 📋 Project Info

| Field | Value |
|-------|-------|
| Package ID | com.getredeemcode.app |
| Version Code | 4 |
| Version Name | 4.0 |
| Min SDK | 24 (Android 7.0) |
| Target SDK | 34 (Android 14) |
| AdMob App ID | ca-app-pub-2366599730777996~6682788999 |
| Gradle Version | 8.9 |
| AGP Version | 8.5.2 |
| Kotlin Version | 2.0.21 |

---

## ⚠️ IMPORTANT NOTES

1. **AdMob App ID** already set hai `AndroidManifest.xml` me
2. **Internet Permission** already set hai
3. **gradlew** already executable hai
4. **ProGuard rules** AdMob ke liye already add kiye hain
5. Pehli baar build me internet chahiye (dependencies download hongi)

---

## ❌ Common Errors & Fix

| Error | Fix |
|-------|-----|
| `SDK location not found` | `local.properties` me `sdk.dir` set karo |
| `Gradle sync failed` | Internet check karo, phir File → Sync Project |
| `Manifest merger failed` | Clean karo: Build → Clean Project |
| `Build → Rebuild Project` | Ye pehle karo agar koi error aaye |

