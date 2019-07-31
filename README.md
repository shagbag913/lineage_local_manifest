# LineageOS fork local manifest

## Why?
I'm just having fun and messing around.

## Platform changes from official LineageOS sources
- Includes Google Pixel alarm, ringtone, notification, and UI sounds
- Google Sans font family used in some areas
- Quick settings vibration when tapping tile
- Minor performance improvements (disabled debugging in some areas)
- Lawnchair launcher included as default launcher
- Slimmed down the power menu

## To sync:
Initialize LineageOS manifest:
```
repo init -u https://github.com/LineageOS/android/ -b lineage-16.0
```

Put this file into .repo/local_manifests (run this from top of Lineage source):
```
curl --create-dirs -o .repo/local_manifests/lineageos_fork.xml https://github.com/shagbag913/lineage_local_manifest
```
